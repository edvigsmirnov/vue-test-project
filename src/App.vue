<template>
  <div class="app">
    <post-form/>
    <post-list :posts="posts"/>
  </div>
</template>

<script>
import PostList from "@/components/PostList";
import PostForm from "@/components/PostForm";

export default {
  components: {
    PostList, PostForm,
  },
  name: "App",
  data() {
    return {
      posts: [
        {id: 1, title: 'Post Title', body: 'Body text'},
        {id: 2, title: 'Post Title 2', body: 'Body text 2'},
        {id: 3, title: 'Post Title 3', body: 'Body text 3'},
      ],
      title: '',
      body: '',
    }
  },
  methods: {
    createPost() {
      const newPost = {
        id: Date.now(),
        title: this.title,
        body: this.body,
      }
      this.posts.push(newPost);
      this.title = '';
      this.body = '';
    },
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  padding: 20px;
}
</style>