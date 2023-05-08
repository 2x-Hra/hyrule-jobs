<template>
    <div class="job-item">
        <ul>
            <li v-for=" job in jobsList" :key="job.id"></li>
        </ul>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    props:{
        jobsList:{
            required: true,
            type: Array
        }
    },
    setup() {
        
    },
})
</script>


<style scoped>

</style>