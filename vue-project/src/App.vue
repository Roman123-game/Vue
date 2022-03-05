
<template>

  <div>
   <post-form />
   <post-list :posts="posts"/>
  </div>
</template>

<script>
import PostList from "@/components/PostList.vue";
import PostForm from "@/components/PostForm.vue";
export default {
  components:{
    PostList,PostForm
  },
  data() {
    return {
      posts: [
        { id: 1, title: "javascript", body: "postDescription 1" },
        { id: 2, title: "javascript", body: "postDescription 2" },
        { id: 3, title: "javascript", body: "postDescription 3" },
      ],
      title: "",
      body: "",
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
    },
  }
}
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

</style>
