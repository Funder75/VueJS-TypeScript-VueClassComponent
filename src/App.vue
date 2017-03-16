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