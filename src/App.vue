<template>
  <div class="app">
    <p>Name - {{ name }}</p>
    <p>Age - {{ age }}</p>
    <button @click="changeName('Marvin')">Change Name</button>
    <button @click="changeAge('30')">Change Age Type String</button>
    <button @click="changeAge(30)">Change Age Type Number</button>

      <p>Name - {{ name }}</p>
  </div>
</template>

<script lang="ts">

// casting age variable as both string or number
// let age: string | number = 25

import { defineComponent, reactive, ref, toRefs } from 'vue';

export default defineComponent({
  name: 'App',
  components: {},
  setup() {

    // using reactive
  //   const state = reactive({
  //     name: 'Link',
  //     age: 25 as string | number 
  //   })
  // // state.name = 98 // does not work as name is a string type and not a number type
  //   state.name = 'Shaun' // works
  //   state.age = 25
  //   return {...toRefs(state) }

  // using refs
  const name = ref('link')
  // const age = ref(25) as number | string // this does not work as it returns a reference value not the actual value
  const age = ref<number | string>(25) // this works using a generic

  age.value = '27' // works
  age.value = 27 // works

    return {name, age}
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
