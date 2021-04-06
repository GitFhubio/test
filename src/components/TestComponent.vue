<template>
  <div>
    <h1> {{post.title}}</h1>
     <button v-on:click="$emit('enlarge-text')">
        Enlarge text
      </button>
          <h2>{{post.content}}</h2>
  </div>
</template>

<script>
export default {
  name: 'TestComponent',
  props: {
    post: Object
  }
}
</script>


<style scoped>

</style>
