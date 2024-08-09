<template>
  <div class="last-posts">
    <h2>Last Posts</h2>
    <button @click="showAllPosts" class="all-posts-button">All Posts</button>
    <div class="posts-container">
      <AllPost
        v-for="post in posts"
        :key="post.id"
        :title="post.title"
        :content="post.content"
        :date="post.date"
      />
    </div>
  </div>
</template>

<script>
import AllPost from './AllPost.vue';


export default {
  name: 'LastPosts',
  components: {
    AllPost,
  },
  data() {
  return {
    posts: [
          {
              id: 1,
            title: 'There are many reasons to get down',
            content: 'The only moment, the only life we have is in the NOW. What happened a few moments or several years ago is gone, what will happen this evening, or next month when we go on holidays is not here yet.',
            date: '10 Oct 21'
          },
          {
              id: 2,
              title: 'Choosing The Right Path',
              content: 'Although this is well intentioned and the goal certainly is to reduce the quantity of these bothersome thoughts, the technique is inherently flawed. Requiring the individual to remember what not to think of infers that they have already thought it. It is akin to telling them to not think of a blue banana.',
              date: '58	Oct 20'
          },
          {
              id: 3,
              title: 'Start your journey here',
              content: 'The only moment, the only life we have is in the NOW. What happened a few moments or several years ago is gone, what will happen this evening, or next month when we go on holidays is not here yet.',
              date: '29	Oct 18'
          },
    ],
  };
},
  methods: {
    showAllPosts() {
      console.log('Showing all posts');
    },
  },
};
</script>

<style lang="scss" scoped>
@import './LastPost'
</style>