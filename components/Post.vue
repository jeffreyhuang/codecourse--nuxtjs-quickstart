<template>
  <div class="post">
    <h1 class="post__title">{{ post.title }}</h1>

    <p>{{ post.body }}</p>
  </div>
</template>

<script>
export default {
  props: {
    post: Object
  }
}
</script>

<style lang="scss">
.post {
  margin-bottom: 40px;

  &__title {
    font-size: 3em;
  }
}
</style>
