<template>
<div>
    <form @submit.prevent>
        <input v-model="post.title" class="input" type="text" placeholder="name" />
        <input v-model="post.body" class="input" type="text" placeholder="body" />
        <button @click='createPost'>Craete</button>

    </form>
</div>
</template>

<script>
export default {
    data() {
        return {
            post: {
                title: '',
                body: '',
            }
        }
    },
    methods: {
        createPost() {

            this.post.id = Date.now();
            this.$emit('create', this.post);
            this.post = {
                title: '',
                body: '',
            }
        }
    }

}
</script>

<style  scoped>

</style>
