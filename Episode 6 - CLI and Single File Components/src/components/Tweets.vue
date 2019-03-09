<template lang="html">
<div class="tweets">
  <input type="text" placeholder="Search" v-model="searchQuery">
  <tweet v-for="tweet, i in filteredTweets" v-bind="tweet" v-bind:key="i" />
</div>
</template>

<script>
import Tweet from './Tweet.vue';

export default {
  name: 'tweets',
  data() {
    return {
      searchQuery: '',
      tweets: [{
          user: 'bob',
          message: 'Hello, I am new',
          liked: ['marc', 'stan']
        },
        {
          user: 'jake',
          message: 'Hello World!',
          liked: []
        },
        {
          user: 'marc',
          message: 'What is up everyone',
          liked: ['jake']
        }
      ]
    }
  },
  computed: {
    filteredTweets() {
      return this.tweets.filter(tweet => tweet.message.toLowerCase()
        .includes(this.searchQuery.toLowerCase()));
    }
  },
  components: {
    Tweet
  }
}
</script>

<style lang="css" scoped>
  .tweets {
    width: 600px;
    margin: 0 auto;
  }

  input {
    display: block;
    margin: 25px auto;
  }
</style>
