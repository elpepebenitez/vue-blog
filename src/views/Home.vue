<template>
  <div class="home">
    <h1>Home</h1>
    <p ref="p" >My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">click me</button>
    <button @click="age++">Add 1 to age</button>
    <input type="text" v-model="name">

  </div>
</template>

<script>
import { ref } from 'vue';
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  setup() {
    console.log('setup');

    const p = ref(null)

    const name = ref('Mario')
    const age = ref(30)

    const handleClick = () => {
      name.value = 'Luigi'
      age.value = '28' 
    }

    return { name, age, handleClick, p }
  }
}
</script>
