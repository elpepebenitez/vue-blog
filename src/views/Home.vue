<template>
  <div class="home">
    <h1>Home</h1>
    <PostList v-if="showPosts" :posts="posts" />
    <button @click="showPosts = !showPosts">toggle posts</button>
    <button @click="posts.pop()" >delete a post</button>
  </div>
</template>

<script>
import { ref,  } from 'vue';
import PostList from '../components/PostList.vue';
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  components: { PostList },
  name: 'Home',
  setup() {
    const posts = ref([
      {title: 'welcome to the blog', body: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Consequuntur illum fugit blanditiis ducimus, perspiciatis est et assumenda sapiente omnis ipsum, delectus distinctio ratione. Vitae, quidem quas recusandae quaerat ratione expedita?', id: 1},
      {title: 'top 5 css tips', body: 'Lorem ipsum', id: 2}
    ])
    const showPosts = ref(true)

    return { posts, showPosts }
  }
}
</script>
