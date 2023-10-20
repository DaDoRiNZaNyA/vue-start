<template>
  <PostItem v-for="post in posts" :key="post.id" :post="post" />
</template>

<script>
import PostItem from "./PostItem.vue";
export default {
  components: {
    PostItem,
  },
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style>
.post {
  padding: 5px;
  border: 2px solid black;
  margin: 5px;
}
</style>
