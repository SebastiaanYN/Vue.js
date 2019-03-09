<template lang="html">
  <div class="likebutton">
    <button v-on:click="like()" v-bind:class="{ hasLiked }">Like!</button>
    <p>{{ liked.length }}</p>
  </div>
</template>

<script>
export default {
  name: 'likebutton',
  props: {
    liked: Array
  },
  computed: {
    hasLiked() {
      return this.liked.includes('me');
    }
  },
  methods: {
    like() {
      if (this.hasLiked) this.liked.splice(this.liked.indexOf('me'), 1);
      else this.liked.push('me');
    }
  }
}
</script>

<style lang="css" scoped>
.likebutton {
  display: flex;
  align-items: center;
  justify-content: center;

  width: 100px;
  height: 30px;
}

button {
  border: 1px solid black;
  outline: none;
  background-color: transparent;
  cursor: pointer;
}

button:hover, .hasLiked {
  background-color: #FF0000
}

p {
  margin: 0 0 0 10px;
}
</style>
