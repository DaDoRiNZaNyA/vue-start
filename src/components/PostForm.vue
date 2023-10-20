<template>
  <div class="post">
    <form class="createPost" @submit.prevent>
      <h4>create</h4>
      <input v-model="post.title" type="text" placeholder="title" />
      <input v-model="post.body" type="text" placeholder="descr" />
      <button @click="createPost">submit</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: "",
        body: "",
      },
    };
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit("create", this.post);
      this.post = {
        title: "",
        body: "",
      };
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
