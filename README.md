# directivue

Lightweight and Optimized **Vue Directives** for your Vue projects

## Available Directives

- **AutoFocus** : Auto focus an element when inserted in the DOM (Safari support)
- **ClickOutside** : Trigger a given function when clicking outside element
- **Ripple** : Trigger a ripple effect when clicking/touching element (Mobile support)

Live Demo : https://directivue.netlify.app

## Installation

```sh
yarn add directivue
# OR
npm install directivue
```

## Usage

```ts
import Vue from 'vue'
import { ClickOutside, Ripple, /* ... */ } from 'directivue'

Vue.directive('clickOutside', ClickOutside)
Vue.directive('ripple', Ripple)
// ...
```

Directives are then accessible in your **Vue** templates as `v-click-outside`, `v-ripple` and so on.

## Nuxt.js


`directivue` needs to be transpiled by Nuxt.js to get benefits of tree-shaking (only the directives you choose will be in your final bundle) :
```js
// nuxt.config.js
export default {
  build: {
    transpile: ['directivue']
  }
}
```
