<template>
  <div class="app">
    <p>{{ name }}</p>
    <p>{{ age }}</p>
    <button @click="changeName('Marvin')">Change Name</button>
    <button @click="changeAge('30')">Change Age Type String</button>
    <button @click="changeAge(30)">Change Age Type Number</button>
  </div>
</template>

<script lang="ts">

// casting age variable as both string or number
// let age: string | number = 25

import { defineComponent } from 'vue';

export default defineComponent({
  name: 'App',
  components: {},
  data(){
    return {
      name: 'Link',
      age: 25 as number | string
    }
  }, 
  methods: {
    changeName(name: string){
      this.name = name
      return name
    },
    changeAge(age: string | number){
      this.age = age
      return age
    }
  }
});
</script>

<style>

</style>
