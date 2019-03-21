<template>
<div id="app">
  <comment
    v-for="item in items"
    v-bind="item"
    v-bind:key="item.id"
  />
  <observer v-on:intersect="intersected" />
</div>
</template>

<script>
import Comment from './components/Comment';
import Observer from './components/Observer';

export default {
  name: 'App',
  components: {
    Comment,
    Observer
  },
  data() {
    return {
      items: [],
      page: 1
    };
  },
  methods: {
    async intersected() {
      const res = await fetch(`https://jsonplaceholder.typicode.com/comments?_page=${this.page++}`);
      const items = await res.json();

      this.items = [...this.items, ...items];
    }
  }
}
</script>

<style>

</style>
