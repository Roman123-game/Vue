<template>
    <div>
 <form @submit.prevent>
      <input
        @input="title = $event.target.value"
        v-bind:value="title"
        class="input"
        type="text"
        placeholder="name"
      />
      <input
        @input="body = $event.target.value"
        v-bind:value="body"
        class="input"
        type="text"
        placeholder="body"
      />

      <button >Craete</button>
    
    
    </form>
    </div>
</template>

<script>

    
</script>

<style  scoped>

</style>