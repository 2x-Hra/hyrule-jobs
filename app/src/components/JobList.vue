<template>
    <div class="job-list">
        <ul>
            <li v-for=" job in jobsList" :key="job.id">
                <h2> {{job.title}} in {{job.location}}</h2>
                <div class="salary">
                    <p> {{ job.salary }}  chooghs </p>
                </div>
                <div class="description">
                    <p>
                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. 
                        Dolorum neque sunt, iusto ab, modi recusandae excepturi aliquam 
                        aliquid odit praesentium dolorem error? Sit modi excepturi voluptas ratione ex perferendis nemo?
                    </p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'
import Job from "../types/Job"

export default defineComponent({
    props:{
        jobsList:{
            required: true,
            type: Array as PropType<Job[]>
        }
    },
    
})
</script>


<style scoped>
  .job-list {
    max-width: 960px;
    margin: 40px auto;
  }
  .job-list ul {
    padding: 0;
 
</style>