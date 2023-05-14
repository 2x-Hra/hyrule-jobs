<template>
  <div class="app">
    <button @click="handleClick('title')">Order by title</button>
    <button @click="handleClick('salary')">Order by Salary</button>
    <button @click="handleClick('location')">Order by location</button>
    <JobListVue :jobsList = "jobs" :orderTerm = "order" />
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs} from 'vue';
import JobListVue from './components/JobList.vue';
import Job from "./types/Job";
import OrderTerm from "./types/OrderTerm";


export default defineComponent({
  name: 'App',
  components: {
    JobListVue
  },
  setup(){
   
      const jobs = ref<Job[]>([
        { title: 'farm worker', location: 'lon lon ranch', salary: 30000, id: '1' },
        { title: 'quarryman', location: 'death mountain', salary: 40000, id: '2' },
        { title: 'flute player', location: 'the lost woods', salary: 35000, id: '3' },
        { title: 'fisherman', location: 'lake hylia', salary: 21000, id: '4' },
        { title: 'prison guard', location: 'gerudo valley', salary: 32000, id: '5' }
      ]);

      const order = ref<OrderTerm>("title");
      const handleClick = ( term : OrderTerm) => {
        order.value = term;
      }

       return ({ jobs , handleClick , order})
    }
   
});
</script>

<style>

</style>
