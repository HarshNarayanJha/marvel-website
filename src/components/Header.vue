<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const activeSection = ref('');

const updateActiveSection = () => {
  const sections = document.querySelectorAll('section');
  const scrollPosition = window.scrollY;

  for (let i = sections.length - 1; i >= 0; i--) {
    const section = sections[i];
    if (scrollPosition >= section.offsetTop - 100) {
      activeSection.value = section.id || '';
      break;
    }
  }
};

onMounted(() => {
  window.addEventListener('scroll', updateActiveSection);
  updateActiveSection();
});

onUnmounted(() => {
  window.removeEventListener('scroll', updateActiveSection);
});
</script>

<template>
  <nav>
    <a href="#"><span :class="{ active: activeSection === 'lead' }">Marvel</span></a>
    <a href="#iron"><span :class="{ active: activeSection === 'iron' }">Iron Man</span></a>
    <a href="#america"><span :class="{ active: activeSection === 'america' }">Captain America</span></a>
    <a href="#thor"><span :class="{ active: activeSection === 'thor' }">Thor</span></a>
    <a href="#strange"><span :class="{ active: activeSection === 'strange' }">Doctor Strange</span></a>
    <a href="#hulk"><span :class="{ active: activeSection === 'hulk' }">Hulk</span></a>
    <a href="#spider"><span :class="{ active: activeSection === 'spider' }">Spider-Man</span></a>
    <a href="#deadpool"><span :class="{ active: activeSection === 'deadpool' }">Deadpool</span></a>
  </nav>
</template>

<style scoped>

nav {
  width: fit-content;
  height: max-content;

  background-color: var(--color-border);
  margin: 0 auto;
  /* border: 0.2px solid var(--color-border-hover); */

  border-radius: 40px;
  padding: 4px;
  justify-content: center;
  align-items: center;
  overflow-x: auto;

  /* display: flex;
  flex-direction: right; */
  

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

  span.active {
    background-color: var(--c-red-dark);
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    color: #fff;
  }


  @media (max-width: 520px) {
    span {
      margin: 0 2px;
      padding: 5px 10px;
    }
  }
}



@media (max-width: 500px) {
  nav {
    font-size: 0.8rem;
    padding: 4px;
    
    width: 100%;
    overflow-x: auto;

    span {
      padding: 2px 8px;
      margin: 2px;
    }
  }
}
</style>
