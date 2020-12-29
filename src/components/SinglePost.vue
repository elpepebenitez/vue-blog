<template>
  <div class="post">
      <h3>{{ post.title }} </h3>
      <p>{{ snippet }}</p>
  </div>
</template>

<script>
import { computed } from 'vue'


export default {
  props: ['post'],
  setup(props) {
      const snippet = computed(() => {
          // substring is a string function that takes 2 argyuments: where to start and where to end. It shows the caracthers in betweet.
          return props.post.body.substring(0 , 50) + '...'
      })

      return { snippet }
  }
}
</script>


<style>
    
</style>