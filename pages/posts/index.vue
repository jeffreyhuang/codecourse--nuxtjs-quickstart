<template>
  <div>
    <Post v-for="post in posts" :key="post.id" :post="post" />
  </div>
</template>

<script>
import axios from 'axios'
import Post from '@/components/Post'

export default {
  components: {
    Post
  },
  layout: 'posts',
  head: {
    title: 'Posts'
  },
  async asyncData () {
    let response = await axios.get('https://jsonplaceholder.typicode.com/posts')

    return {
      posts: response.data
    }
  }
}
</script>
