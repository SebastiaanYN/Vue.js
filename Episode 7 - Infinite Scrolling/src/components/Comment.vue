<template>
<div class="comment">
  <h1>{{ name }}</h1>
  <p>{{ body }}</p>
</div>
</template>

<script>
export default {
  name: 'comment',
  props: {
    postId: Number,
    id: Number,
    name: String,
    email: String,
    body: String
  }
}
</script>

<style scoped>

</style>
