<script setup></script>

<template>
  <nav>
    <a href="#"><span class="first">Marvel</span></a>
    <a href="#features"><span class="">Features</span></a>
    <a href="#usage"><span class="">Usage</span></a>
    <a href="#privacy"><span class="">Privacy</span></a>
    <a href="#about"><span>About</span></a>
  </nav>
</template>

<style scoped>
img.icon {
  max-width: 30px;
  margin-top: 7px;
}

nav {
  width: fit-content;
  height: max-content;

  background-color: var(--color-border);
  /* border: 0.2px solid var(--color-border-hover); */

  border-radius: 40px;
  padding: 4px;

  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);

  span {
    display: inline-block;
    width: fit-content;
    height: max-content;

    margin: 0 5px;
    padding: 5px 20px;
    border-radius: 40px;

    color: var(--color-text);

    transition: all 0.5s ease-in-out;
  }

  span.first {
    background-color: var(--c-green-dark);
    font-weight: 900;
    font-family: "Baloo 2";
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
