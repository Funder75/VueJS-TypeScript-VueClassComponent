# VueJS TypeScript VueClassComponent

> Boilerplate project setup with VueJS 2, TypeScript, WebPack 2 and Vue Class Component.

Build Vue JS 2 apps using TypeScript in single file components. Setup with Webpack 2 and hot load.

Based of variuos examples:

- [Writing Class-Based Components with Vue.js and TypeScript](https://alligator.io/vuejs/typescript-class-components/).
- [ES / TypeScript decorator for class-style Vue components.](https://github.com/vuejs/vue-class-component).

### Example

Following is the example written in Babel. If you are looking for TypeScript version, [it's in the example directory](example/App.vue).

``` vue
<template>
  <div>
    <p>Long-form v-model example {{myDataProperty}}</p>
    <input :value="myDataProperty" @input="updateMyProperty($event)"/>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { Component } from 'vue-property-decorator'

@Component
export default class App extends Vue {
  // Data property


  myDataProperty: string = "";

  // Lifecycle hook
  mounted () {
    this.myDataProperty = 'Mounted'
  }

  // Component method
  updateMyProperty ($event : any) {
    this.myDataProperty = $event.target.value
  }
}
</script>
```

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```


