<template>
  <div class="post">
    <div><strong>title: </strong>{{ post.title }}</div>
    <div><strong>desc: </strong>{{ post.body }}</div>
    <button>delete</button>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      title: String,
      body: String,
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
