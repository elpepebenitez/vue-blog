<template>
  <div class="home">
    <h1>Home</h1>
    <p ref="p" >My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">click me</button>

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

    let name = 'Pepe'
    let age = 30

    const handleClick = () => {
      console.log(p, p.value)
      p.value.classList.add('test')
      p.value.textContent = 'Hello'
    }

    return { name, age, handleClick, p }
  }
}
</script>
