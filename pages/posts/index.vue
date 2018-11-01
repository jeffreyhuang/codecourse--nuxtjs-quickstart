<template>
  <p>{{ posts }}</p>
</template>

<script>
import axios from 'axios'

export default {
  async asyncData () {
    let response = await axios.get('https://jsonplaceholder.typicode.com/posts')

    return {
      posts: response.data
    }
  }
}
</script>
