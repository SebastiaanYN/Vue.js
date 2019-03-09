<template lang="html">
  <nav>
    <h1>Tweeter</h1>
  </nav>
</template>

<script>
export default {
  name: 'navbar'
}
</script>

<style lang="css" scoped>
  nav {
    background-color: lightgrey;
    width: 100%;
    height: 50px;

    display: flex;
    align-items: center;
  }

  h1 {
    margin: 0 0 0 25px;
  }
</style>
