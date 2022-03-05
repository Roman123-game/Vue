<template>
<div class='postList'>
    <div>spisok polzovatelei</div>
    <post-task :post="post" v-for="post in posts"/>
 
</div>
<div class='post__btn'>
<button class ='btn'>udalit</button>

</div>
</template>

<script>
import PostTask from "./PostTask.vue";
export default {
    components : {PostTask},
    props: {
        posts: {
            type: Array,
            required: true,
        }
    }
}
</script>

<style >
.postList{
    padding:5px;
}
</style>
