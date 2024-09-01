<script setup>
defineProps({
  name: {
    type: String,
    required: true
  },
  about: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div>
    <h1>{{ name }}</h1>
    <p>{{ about }}</p>
  </div>
</template>

<style scoped>

div {
  margin: 3em 2em;
  padding: 1em 2em;


  border: 1px solid red;
}

</style>
