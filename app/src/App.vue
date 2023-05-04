<template>
  <div class="app">
    Hello , {{ name }}
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs} from 'vue';


export default defineComponent({
  name: 'App',
  components: {
    
  },
  setup(){
      // const state = reactive({
      //   name : "link",
      //   age  : 25
      // })
      // return({
      //   ...toRefs(state)        
      // })
      
    }
});
</script>

<style>

</style>
