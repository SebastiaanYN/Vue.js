<template>
  <div id="app">
    <app-navbar />
    <router-view />
    <app-footer />
  </div>
</template>

<script>
import AppNavbar from './components/AppNavbar';
import AppFooter from './components/AppFooter';

export default {
  name: 'App',
  components: {
    AppNavbar,
    AppFooter,
  },
};
</script>

<style>

</style>
