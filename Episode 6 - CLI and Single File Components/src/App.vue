<template>
<div id="app">
  <app-navbar />
  <tweets />
</div>
</template>

<script>
import AppNavbar from './components/AppNavbar.vue';
import Tweets from './components/Tweets.vue';

export default {
  name: 'App',
  components: {
    AppNavbar,
    Tweets
  }
}
</script>

<style>
html,
body {
  margin: 0;
  padding: 0;
}
</style>
