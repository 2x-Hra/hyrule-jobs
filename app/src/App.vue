<template>
  <div class="app">
    <button>Order by title</button>
    <button>Order by Salary</button>
    <button>Order by location</button>
    <JobListVue :jobsList = "jobs" />
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs} from 'vue';
import JobListVue from './components/JobList.vue';
import Job from "./types/Job"


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

       return ({ jobs })
    }
   
});
</script>

<style>

</style>
