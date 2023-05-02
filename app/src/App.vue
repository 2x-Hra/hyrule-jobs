<template>
  <div class="app">
    Hello , {{ name }}
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs} from 'vue';
import Job from "./types/Job"

export default defineComponent({
  name: 'App',
  components: {
    
  },
  setup(){
    // ~~~~~~~~~~~~~~~~~~~~~~~   1st style  ~~~~~~~~~~~~~~~~~~ //

      // const state = reactive({
      //   name : "link",
      //   age  : 25 as string | number
      // })
      // state.age = 33
      // return({
      //   ...toRefs(state)        
      // })

      // ~~~~~~~~~~~~~~~~~~~~~~~   2nd style  ~~~~~~~~~~~~~~~~~~ //
       
      // const name = ref("link");
      // const age = ref<string | number>(25);
      
      // return ({
      //   name,
      //   age
      //   })
    }
});
</script>

<style>

</style>
