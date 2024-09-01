<script setup>
import Header from "./components/Header.vue";
import CharSection from "./components/CharSection.vue";
</script>

<template>
  <header>
    <Header />
  </header>

  <section>
    <CharSection name="Iron Man" about="..." />
  </section>
  <section>
    <CharSection name="Iron Man" about="..." />
  </section>
  <section>
    <CharSection name="Iron Man" about="..." />
  </section>
  <section>
    <CharSection name="Iron Man" about="..." />
  </section>
  <section>
    <CharSection name="Iron Man" about="..." />
  </section>
</template>

<style scoped>
header {
  line-height: 1.5;
  display: flex;
  justify-content: center;
  align-items: center;
  position: sticky;
  top: 10px;

  margin-bottom: 2em;

  background: red;
}

section {
  min-height: 100svh;
  min-width: 100svw;
  display: flex;
  scroll-behavior: smooth;

  scroll-snap-align: start;
  scroll-margin-top: 150px;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
