<template>
  <div class="post-list">
      <div v-for="post in posts" :key="post.id">
          <single-post :post="post"/>
      </div>
  </div>
</template>

<script>
import SinglePost from "./SinglePost.vue"


export default {
    components: { SinglePost },
    props: ['posts'],
    setup(props) {},
}
</script>


<style>
    
</style>