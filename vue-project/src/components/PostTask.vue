<template>
<div class='post'>
    <div >{{post.title}}</div>
    <div >{{post.body}}</div>
</div>
</template>

<script>

export default {
    
    props: {
        post: {
            type: Object,
            required: true,
        }
    }
}
</script>

<style >
.post {
  padding: 15px;
  border: 1px solid red;
  margin-top: 15px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.post__btns {
  display: flex;
}
</style>
