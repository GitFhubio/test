<template>
  <div>
    <h1> {{post}}</h1>
    <h2>{{content}}</h2>
  </div>
</template>

<script>
export default {
  name: 'TestComponent',
  props: {
    post: String,
    content:String
  }
}
</script>


<style scoped>

</style>
