<template>
  <div id="app">
    <input v-model.trim="search" type="search" placeholder="Search">
    <router-view />
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      search: '',
    };
  },
  watch: {
    search(q) {
      this.$router.push({ name: 'search', query: { q } });
    },
  },
};
</script>

<style>

</style>
