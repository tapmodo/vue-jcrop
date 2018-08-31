<template>
  <div v-once/>
</template>

<script>
import Jcrop from 'jcrop';

export default {
  name: 'Jcrop',
  props: [ 'src', 'options' ],
  mounted: function() {
    const img = new Image();
    this.$el.appendChild(img);
    img.src = this.src;
    Jcrop.load(img).then(this.startup);
  },
  methods: {
    startup(img){
      console.log(this.options);
      this.jcrop = Jcrop.attach(img,this.options||{});
      const rect = Jcrop.Rect.sizeOf(this.jcrop.el);
      this.jcrop.listen('crop.update',widget => this.$emit('update',widget));
      this.jcrop.listen('crop.activate',widget => this.$emit('activate',widget));
      this.jcrop.listen('crop.remove',widget => this.$emit('remove',widget));
      this.jcrop.newWidget(rect.scale(.7,.5).center(rect.w,rect.h));
      this.pos = this.jcrop.pos;
      this.jcrop.focus();
    }
  },
  watch: {
    options: {
      handler: function(o) { this.jcrop.setOptions(o); },
      deep: true
    }
  },
  destroyed: () => {
  },
  data: () => ({
    pos: null,
    jcrop: null
  })
}
</script>

<style lang="scss">
@import "~jcrop/build/css/jcrop.scss";
</style>
