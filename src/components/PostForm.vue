<template>
  <form @submit.prevent>
    <h4>Create new post</h4>
    <input
        v-bind:value="title"
        @input="title = $event.target.value"
        class="input"
        type="text"
        placeholder="Post name">
    <input
        v-bind:value="body"
        @input="body = $event.target.value"
        class="input"
        type="text"
        placeholder="Post description">
    <button class="btn">Add post</button>
  </form>
</template>

<script>
export default {
  name: "PostForm"
}
</script>

<style scoped>
.input {
  width: 100%;
  border: 1px solid teal;
  padding: 15px 15px;
  margin-top: 15px;
}
.btn {
  align-self: flex-start;
  margin-top: 15px;
  padding: 10px 15px;
  background: none;
  color: teal;
  border: 1px solid teal;
}
form {
  display: flex;
  flex-direction: column;
}
</style>