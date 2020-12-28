<template>
  <div class="home">
    <h1>Home</h1>
    <p>My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">click me</button>

  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  setup() {
    console.log('setup');

    let name = 'Pepe'
    let age = 30

    const handleClick = () => {
      console.log('you clicked me')
    }

    return { name, age, handleClick }
  }
}
</script>
