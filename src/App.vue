<template>
  <div id="app">
    <div style="height: 500px; width: 500px; border: 1px solid red; position: relative;">
      <vue-draggable-resizable @contextmenu ='contextmenu' :itemdata ='item'  v-for="(item, index) in datao" :key = 'index' :w="400" :h="400" :parent="true" :min-width="200" :min-height="200" :ref="'sss'+ index">
        <p>vue-draggable-resizable</p>
      </vue-draggable-resizable>
    </div>
  </div>
</template>

<script>
import VueDraggableResizable from './components/vue-draggable-resizable'
import './components/vue-draggable-resizable.css'

export default {
  name: 'app',
  components: {
    VueDraggableResizable
  },
  data: function () {
    return {
      datao: [
        {
          id: 1
        },
        {
          id: 2
        }
      ]
    }
  },
  methods: {
    contextmenu (data, e) {
    }
  }
}
</script>

<style>
  .vdr {
    border: 1px dashed black;
  }
</style>
