<template>
  <div class="app">
    <PostForm @create="createPost" />
    <PostList :posts="posts" />
  </div>
</template>

<script>
import PostForm from "./components/PostForm";
import PostList from "./components/PostList";
export default {
  components: {
    PostList,
    PostForm,
  },
  data() {
    return {
      posts: [
        { id: 1, title: "qwerty", body: "qwertyqwerty" },
        { id: 2, title: "ewqewq", body: "ewqewqewqeqw" },
      ],
    };
  },
  methods: {
    createPost(post) {
      this.posts.push(post);
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: 0;
}
.post {
  padding: 5px;
  border: 2px solid black;
  margin: 5px;
}
.createPost {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  height: 15vh;
}
</style>
