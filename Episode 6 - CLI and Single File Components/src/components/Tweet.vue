<template lang="html">
<div class="tweet">
  <h1>{{ user }}</h1>
  <p>{{ message }}</p>
  <like-button v-bind:liked="liked" />
</div>
</template>

<script>
import LikeButton from './LikeButton';

export default {
  name: 'tweet',
  props: {
    user: String,
    message: String,
    liked: Array
  },
  components: {
    LikeButton
  }
}
</script>

<style lang="css" scoped>
.tweet {
  border-bottom: 1px solid black;
}
</style>
