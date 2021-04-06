<template>
  <div>
    <h1> {{post.title}}</h1>
     <button v-on:mouseenter="$emit('color-text')" v-on:mouseleave="$emit('color-text2')">
        change color
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
