<script setup></script>

<template>
  <nav>
    <a href="#"><span class="first">Marvel</span></a>
    <a href="#iron"><span class="">Iron Man</span></a>
    <a href="#america"><span class="">Captain America</span></a>
    <a href="#thor"><span class="">Thor</span></a>
    <a href="#strange"><span>Doctor Strange</span></a>
    <a href="#hulk"><span>Hulk</span></a>
    <a href="#spider"><span>Spider-Man</span></a>
    <a href="#deadpool"><span>Deadpool</span></a>
  </nav>
</template>

<style scoped>

nav {
  width: fit-content;
  height: max-content;

  background-color: var(--color-border);
  border: 0.2px solid var(--color-border-hover);

  border-radius: 40px;
  padding: 4px;

  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);

  span {
    display: inline-block;
    width: fit-content;
    height: max-content;

    margin: 0 1px;
    padding: 5px 15px;
    border-radius: 40px;

    color: var(--color-text);

    transition: all 0.5s ease-in-out;
  }

  span.first {
    background-color: var(--c-red-dark);
    font-weight: 900;
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    color: #fff;
  }

  span.active:not(.first) {
    background-color: var(--color-border-hover);
    color: #fff;
  }

  @media (max-width: 520px) {
    span {
      margin: 0 2px;
      padding: 5px 10px;
    }
  }
}

.links {
  max-width: 30px;
  margin-top: 12px;
}

@media (max-width: 500px) {
  nav {
    font-size: 0.8rem;
    padding: 4px;

    span {
      padding: 2px 8px;
      margin: 2px;
    }
  }
}
</style>
