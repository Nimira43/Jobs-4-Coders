<script setup>

import JobListing from './JobListing.vue'
import jobData from '@/jobs.json'
import { ref } from 'vue'

const jobs = ref(jobData)
console.log(jobs.value) 

</script>

<template>
  <section class='bg-[#1c9fd3] px-4 py-10'>
    <div class='container-xl lg:container m-auto'>
      <h2 class='text-3xl font-bold text-[#eee] mb-6 text-center'>
        Browse Jobs
      </h2>
      <div class='grid grid-cols-1 md:grid-cols-3 gap-6'>
        <JobListing v-for='job in jobs' :key='job.id' :job='job' />
        
      </div>
    </div>
  </section>
</template>