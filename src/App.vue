<script setup>
import Header from "./components/Header.vue";
import SectionLead from "./components/SectionLead.vue";
import CharSection from "./components/CharSection.vue";
</script>

<template>
  <header>
    <Header />
  </header>

  <section id="lead">
    <SectionLead />
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
  <section>
    <CharSection name="Iron Man" about="..." />
  </section>
</template>

<style scoped>
header {
  line-height: 1.5;
  position: sticky;
  top: 10px;
  justify-content: space-around;
  align-items: start;
  display: flex;

  margin-bottom: 2em;

  /* background: red; */
}

section#lead {
  min-height: 80svh;
  display: flex;
  flex-direction: column;
  justify-content: start;
}

section {
  min-height: 100svh;
  margin: 80px 0;

  scroll-behavior: smooth;

  scroll-snap-align: start;
  scroll-margin-top: 75px;

  /* border: 1px solid green; */
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
