<template>
<div>
    <post-form @create="createPost" />
    <post-list :posts="posts" />
  
</div>
</template>

<script>
import PostList from "@/components/PostList.vue";
import PostForm from "@/components/PostForm.vue";
import PostTask from "@/components/PostTask.vue"
export default {
    components: {
        PostList,
        PostForm,
         PostTask,

    },
    data() {
        return {
            posts: [{
                    id: 1,
                    title: "javascript",
                    body: "postDescription 1"
                },
                {
                    id: 2,
                    title: "javascript",
                    body: "postDescription 2"
                },
                {
                    id: 3,
                    title: "javascript",
                    body: "postDescription 3"
                },
            ],

        }
    },
    methods: {
        createPost(post) {
            this.posts.push(post);
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
