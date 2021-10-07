<template>
  <div class="app">
  </div>
</template>

<script lang="ts">

// casting age variable as both string or number
// let age: string | number = 25

import { defineComponent, reactive, toRefs } from 'vue';

export default defineComponent({
  name: 'App',
  components: {},
  setup() {
    const state = reactive({
      name: 'Link',
      age: 25 as string | number 
    })

    return {...toRefs(state) }
  }
});
</script>

<style>

</style>
