<template>
<div>
    <div class="post" :key="post.id" v-for="post in posts">
        <div>{{ post.title }}</div>
        <div>{{ post.body }}</div>
    </div>
</div>
</template>

<script>
export default {
    props: {
        posts: {
            type: Array,
            required: true,
        }
    }
}
</script>

<style scoped>
.post {
    padding: 10px;
    margin: 5px;
    border: 1px solid red;
}
</style>
