<script setup>
import { ref, onMounted, onUnmounted } from "vue";
import { gsap } from "gsap";

onMounted(() => {
  const image = document.querySelector("img#logo");
  gsap.from(image, {
    y: -500,
    duration: 0.4,
    delay: 0.5,
    ease: "in",
  });

  gsap.from("#welcome", {
    opacity: 0.0,
    duration: 4,
    delay: 1.2,
    ease: "elastic"
  });

  gsap.from("#lead-body", {
    scaleX: 0,
    duration: 0.25,
    delay: 1.7,
    ease: "back"
  });
});
</script>

<template>
  <div>
    <img rel="preload" priority="high" id="logo" src="/marvel.png" draggable="false" />
    <p id="welcome">Welcome to the Universe</p>
  </div>
  <p id="lead-body">
    The Marvel universe is a vast and wondrous place, full of iconic characters, epic battles, and unforgettable storylines.
    From the humble beginnings of Stan Lee's first comic book creations to the modern-day blockbusters that dominate the box
    office, Marvel has consistently pushed the boundaries of what's possible in the world of superheroes. With a diverse cast
    of characters that includes the likes of Iron Man, Captain America, Black Widow, and the Hulk, there's something for
    everyone in the Marvel universe. Whether you're a lifelong fan or just discovering the magic of Marvel, the intricate web
    of interconnected stories and characters is sure to captivate and inspire. With new movies, TV shows, and comic books
    being released all the time, the Marvel universe is constantly evolving and expanding, offering endless opportunities for
    fans to engage with their favorite characters and storylines.
  </p>
</template>

<style scoped>
div {
  margin: 3em 2em;
  padding: 1em 2em;

  display: flex;
  flex-direction: column;
  align-items: center;

  /* border: 1px solid blue; */

  img {
    max-width: 45%;
    /* mix-blend-mode: color-burn; */
  }

  h1 {
    font-size: 7rem;
    line-height: 8rem;
    font-weight: 900;
    color: var(--color-text-bright);
  }

  p {
    margin-top: 1em;
    font-size: 1.4rem;
    line-height: 2rem;
    font-weight: 600;
    color: var(--color-text);
  }
}

p {
  font-size: 1.5rem;
  line-height: 2.5rem;
  margin: 0 2em;
  padding: 0.5em 0.1em;
  text-align: justify;
  font-weight: 500;
  color: var(--color-text-bright);
}
</style>
