<template>
  <div class="app">
    <p>{{ jobs[0].location }}</p>
  </div>
</template>

<script lang="ts">

// casting age variable as both string or nu mber
// let age: string | number = 25

import { defineComponent, reactive, ref, toRefs } from 'vue';
import Job from './types/job'

export default defineComponent({
  name: 'App',
  components: {},
  setup() {
    
    const jobs = ref<Job[]>([
      { title: 'farm worker', location: 'Ion Ion Ranch', salary: 30000, id: '1' },
      { title: 'quarryman', location: 'death mountain', salary: 40000, id: '2' },
      { title: 'flute player', location: 'the lost woods', salary: 35000, id: '3' },
      { title: 'fisherman', location: 'lake hylia', salary: 21000, id: '4' },
      { title: 'prison guard', location: 'gerudo valley', salary: 32000, id: '5' }
    ])

    return  { jobs }
  },
  methods: {

  }
});
</script>

<style>

</style>
