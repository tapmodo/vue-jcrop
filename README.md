# vue-jcrop

[![npm](https://img.shields.io/npm/v/vue-jcrop.svg) ![npm](https://img.shields.io/npm/dm/vue-jcrop.svg)](https://www.npmjs.com/package/vue-jcrop)
[![vue2](https://img.shields.io/badge/vue-2.x-brightgreen.svg)](https://vuejs.org/)

The Javascript cropping widget for Vue.js

## Table of contents

- [Installation](#installation)
- [Usage](#usage)
- [Example](#example)

# Installation

```
npm install --save vue-jcrop
```

## Default import

Install all the components:

```javascript
import Vue from 'vue'
import VueJcrop from 'vue-jcrop'

Vue.use(VueJcrop)
```

Use specific components:

```javascript
import Vue from 'vue'
import { Jcrop } from 'vue-jcrop'

Vue.component('Jcrop', Jcrop)
```

**⚠️ A css file is included when importing the package. You may have to setup your bundler to embed the css in your page.**

## Distribution import

Install all the components:

```javascript
import 'vue-jcrop/dist/vue-jcrop.css'
import VueJcrop from 'vue-jcrop/dist/vue-jcrop.common'

Vue.use(VueJcrop)
```

Use specific components:

```javascript
import 'vue-jcrop/dist/vue-jcrop.css'
import { Jcrop } from 'vue-jcrop/dist/vue-jcrop.common'

Vue.component('Jcrop', Jcrop)
```

**⚠️ You may have to setup your bundler to embed the css file in your page.**

## Browser

```html
<link rel="stylesheet" href="vue-jcrop/dist/vue-jcrop.css"/>

<script src="vue.js"></script>
<script src="vue-jcrop/dist/vue-jcrop.browser.js"></script>
```

The plugin should be auto-installed. If not, you can install it manually with the instructions below.

Install all the components:

```javascript
Vue.use(VueJcrop)
```

Use specific components:

```javascript
Vue.component('Jcrop', VueJcrop.Jcrop)
```

## Source import

Install all the components:

```javascript
import Vue from 'vue'
import VueJcrop from 'vue-jcrop/src'

Vue.use(VueJcrop)
```

Use specific components:

```javascript
import Vue from 'vue'
import { Jcrop } from 'vue-jcrop/src'

Vue.component('Jcrop', Jcrop)
```

**⚠️ You need to configure your bundler to compile `.vue` files.** More info [in the official documentation](https://vuejs.org/v2/guide/single-file-components.html).

# Usage

> TODO

# Example

> TODO

---

# Plugin Development

## Installation

The first time you create or clone your plugin, you need to install the default dependencies:

```
npm install
```

## Watch and compile

This will run webpack in watching mode and output the compiled files in the `dist` folder.

```
npm run dev
```

## Use it in another project

While developping, you can follow the install instructions of your plugin and link it into the project that uses it.

In the plugin folder:

```
npm link
```

In the other project folder:

```
npm link vue-jcrop
```

This will install it in the dependencies as a symlink, so that it gets any modifications made to the plugin.

## Publish to npm

You may have to login to npm before, with `npm adduser`. The plugin will be built in production mode before getting published on npm.

```
npm publish
```

## Manual build

This will build the plugin into the `dist` folder in production mode.

```
npm run build
```

---

## License

[MIT](http://opensource.org/licenses/MIT)
