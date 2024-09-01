<script setup>
defineProps({
  name: {
    type: String,
    required: true,
  },
  about: {
    type: String,
    required: true,
  },
  photo: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div>
    <div class="heading">
      <div class="stats">
        <h1>{{ name }}</h1>
        <ul>
          <li>Height:</li>
          <li>Weight:</li>
        </ul>
      </div>
      <img :src="photo" :alt="`picture of ${name}`" />
    </div>
    <p>{{ about }}</p>
  </div>
</template>

<style scoped>
div {
  margin: 3em 2em;
  /* padding: 1em 2em; */

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  div.heading {
    display: flex;
    flex-direction: row;
    justify-content: space-between;

    div.stats {
      h1 {
        font-size: 3rem;
        font-weight: 600;
        color: var(--color-text-bright);
      }

      ul {
        width: 100%;
        padding: 0 2em;
        /* border: 1px solid green; */
      }
    }
  }

  img {
    max-width: 30%;
    align-self: end;
  }

  p {
    font-size: 1.2rem;
    text-align: justify;
  }

  /* border: 1px solid red; */
}
</style>
