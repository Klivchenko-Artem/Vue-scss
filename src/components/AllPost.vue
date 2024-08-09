<template>
  <div class="post-card">
    <div class="post-image">
    <img src="../img/post.jpg" alt="Post Image"  />
    </div>
    <div class="post-content">
      <h3 class="post-title">{{ title }}</h3>
      <p class="post-text">{{ content }}</p>
      <div class="post-footer">
        <span class="post-date">{{ date }}</span>
        <a href="#" class="read-more-link">Read more</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PostCard',
  props: {
    title: String,
    content: String,
    date: String,
  },
};
</script>

<style lang="scss" scoped>
@import "./AllPost"

</style>