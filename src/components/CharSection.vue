<script setup>
const props = defineProps({
  heroId: {
    type: String,
    required: true,
  },
  name: {
    type: String,
    required: true,
  },
  about: {
    type: String,
    required: true,
  },
  realName: {
    type: String,
    required: true,
  },
  alias: {
    type: String,
    required: true,
  },
  quote: {
    type: String,
    required: true,
  },
  origin: {
    type: String,
    required: true,
  },
  photo: {
    type: String,
    required: true,
  },
  width: {
    type: String,
    required: false,
    default: "30%",
  },
  margin: {
    type: String,
    required: false,
    default: "0px",
  },
  color: {
    type: String,
    required: false,
    default: "black",
  },
  hoverColor: {
    type: String,
    required: false,
    default: "black",
  },
});

import { gsap } from "gsap";
import { ref, onMounted, onUnmounted } from "vue";

onMounted(() => {
  const image = document.querySelector(`.img-lead-${props.heroId}`);
  const text = document.querySelector(`.about-${props.heroId}`);

  gsap.from(image, {
    x: 500,
    opacity: 0,
    scrollTrigger: {
      trigger: `.img-lead-${props.heroId}`,
      start: "top 50%",
      end: "bottom 80%",
      scrub: true,
    },
  });

  gsap.from(text, {
    opacity: 0,
    scrollTrigger: {
      trigger: `.about-${props.heroId}`,
      start: "top 90%",
      end: "bottom 100%",
      scrub: true,
      markers: false
    },
  });

  gsap.from(`#name-${props.heroId}`, {
    scaleX: 0,
    ease: "back",
    scrollTrigger: {
      trigger: `#name-${props.heroId}`,
      start: "top 80%",
      end: "bottom 80%",
      scrub: true,
    },
  });
});
</script>

<template>
  <div>
    <div class="heading">
      <div class="stats">
        <h1 :id="`name-${heroId}`">{{ name }}</h1>
        <small>{{ realName }}</small>
        <ul>
          <li>Alias: {{ alias }}</li>
          <li>Origin: {{ origin }}</li>
        </ul>
        <i>{{ quote }}</i>
      </div>
      <img :class="`img-lead-${heroId}`" :src="photo" :alt="`picture of ${name}`" draggable="false" />
    </div>
    <p :class="`about-${heroId}`">{{ about }}</p>
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
    width: 100%;

    div.stats {
      h1 {
        font-size: 4.5rem;
        line-height: 6rem;
        font-weight: 600;
        color: var(--color-text-bright);
        z-index: 500;
      }

      small {
        font-size: 1.2rem;
        margin-bottom: 2.5em;
        color: var(--c-text);
      }

      ul {
        width: 100%;
        padding: 0 2em;
        color: var(--color-text-bright);
        font-size: 1.1rem;
        list-style-type: square;
      }

      i {
        margin-top: 1em;
        font-size: 1.2rem;
      }
    }

    img {
      --shadow-color: v-bind(color);
      --shadow-color-hover: v-bind(hoverColor);
      max-width: v-bind(width);
      align-self: end;
      margin-right: v-bind(margin);
      filter: drop-shadow(0rem 0rem 0.8rem var(--shadow-color));
      transition: filter ease-in-out 0.2s;
      z-index: 500;
    }

    img:hover {
      filter: drop-shadow(0rem 0rem 0.8rem var(--shadow-color-hover));
    }
  }

  p {
    font-size: 1.2rem;
    text-align: justify;
    color: var(--color-text-bright);
  }
}
</style>
