<script setup>
import Header from "./components/Header.vue";
import SectionLead from "./components/SectionLead.vue";
import CharSection from "./components/CharSection.vue";

import gsap from "gsap";

import { onMounted } from "vue";

onMounted(() => {
  window.addEventListener("mousemove", (e) => {
    const isTargetLinkOrHd = e.target.closest("img") || e.target.closest("h1");
    const isP = e.target.closest("p");
    gsap.to(".cursor-follower", {
      x: e.clientX,
      y: e.clientY,
      duration: 0.2,
      width: `${isP ? "5px" : "20px"}`,
      height: `${isP ? "30px" : "20px"}`,
      borderRadius: `${isP ? "0" : "100%"}`,
      transform: `scale(${isTargetLinkOrHd ? 3 : 1})`,
    });
  });
});
</script>

<template>
  <header>
    <Header />
  </header>
  <div class="cursor-follower"></div>
  <section id="lead">
    <SectionLead />
  </section>
  <section id="iron">
    <CharSection
      heroId="iron"
      photo="iron-man.png"
      width="40%"
      name="Iron Man"
      about="Iron Man, aka Tony Stark, is a founding member of the Avengers and one of the most iconic characters in the Marvel universe. A billionaire inventor and philanthropist, Tony Stark created the Iron Man suit to save his own life and later used it to fight crime and protect the world from various threats. With his wit, intelligence, and advanced technology, Iron Man has become a beloved and respected superhero, known for his sarcastic humor and unwavering commitment to justice."
      realName='Anthony Edward "Tony" Stark'
      alias="None"
      origin="Long Island, New York"
      quote="Genius, Billionaire, Philanthropist"
      hoverColor="red"
    />
  </section>
  <section id="america">
    <CharSection
      heroId="america"
      photo="captain-hero.png"
      width="40%"
      name="Captain America"
      realName="Steve Rogers"
      about="Captain America, aka Steve Rogers, is a patriotic superhero and one of the most respected members of the Avengers. Created during World War II as part of a secret government experiment, Steve Rogers was transformed into a super-soldier with enhanced strength, agility, and endurance. With his indestructible shield and unwavering commitment to justice, Captain America has fought against tyranny and oppression, becoming a symbol of hope and freedom for generations of Americans. His strong moral compass and old-fashioned values have earned him the respect and admiration of his fellow Avengers and the public alike."
      origin="Brooklyn"
      alias="Cap"
      quote="I don't like bullies; I don't care where they're from"
      hoverColor="skyblue"
    />
  </section>
  <section id="thor">
    <CharSection
      heroId="thor"
      photo="thor-hero.png"
      width="50%"
      name="Thor"
      realName="Thor"
      about="Thor is the Norse god of thunder and a founding member of the Avengers. With his incredible strength, lightning powers, and indestructible hammer Mjolnir, Thor has become a powerful force for justice and protection in the Marvel universe. As the son of Odin, the king of Asgard, Thor has a deep sense of duty and responsibility, but his arrogance and impulsiveness have also led to conflicts with his fellow Avengers. Despite this, Thor's bravery, loyalty, and sense of humor have made him a beloved and integral member of the team."
      origin="Asgard"
      quote="You People Are So Petty. And Tiny."
      alias="None"
      hoverColor="grey"
    />
  </section>
  <section id="strange">
    <CharSection
      heroId="strange"
      photo="strange-hero.png"
      width="40%"
      name="Doctor Strange"
      realName="Dr. Stephen 'Vincent' Strange"
      about="Doctor Strange, aka Stephen Strange, is a sorcerer and a master of the mystic arts. Once a brilliant and arrogant neurosurgeon, Strange's life was forever changed when a car accident left his hands crippled. Desperate to regain the use of his hands, Strange sought out the Ancient One, a powerful sorcerer who taught him the mystic arts. With his newfound abilities, Strange became the Sorcerer Supreme, protecting the Earth from magical threats and other-dimensional entities."
      origin="Philadelphia, Pennsylvania"
      alias="Sorcerer Supreme, Master of the Mystic Arts"
      quote="If I tell you what happens, it won't happen."
      hoverColor="darkred"
    />
  </section>
  <section id="hulk">
    <CharSection
      heroId="hulk"
      photo="hulk-hero.png"
      name="Hulk"
      width="35%"
      about="The Hulk, aka Bruce Banner, is a brilliant scientist who, due to exposure to gamma radiation, transforms into a giant, green-skinned monster with incredible strength and durability whenever he becomes angry or experiences strong emotions. As the Hulk, he has clashed with the military, other superheroes, and even himself, as he struggles to maintain control over his alter ego. Despite his destructive tendencies, the Hulk has also been a valuable member of the Avengers, using his incredible powers to protect the world from threats too great for mortal men."
      realName="Robert Bruce Banner"
      origin="Dayton, Ohio"
      alias="Green One"
      quote="No Banner, Only Hulk!"
      hoverColor="lightgreen"
    />
  </section>
  <section id="spider">
    <CharSection
      heroId="spider"
      photo="spiderman-hero.png"
      width="45%"
      margin="-5em"
      name="Spider-Man"
      about="Spider-Man, aka Peter Parker, is a teenage nerd-turned-superhero who gained incredible powers after being bitten by a radioactive spider. With his powers, he fights crime and battles supervillains in New York City, all while balancing his personal life and keeping his secret identity hidden from the world. With his quick wit, agility, and web-slinging abilities, Spider-Man has become a beloved and iconic superhero, known for his catchphrase 'With great power comes great responsibility.'"
      realName="Peter Parker"
      origin="Queens, New York"
      alias="Night Monkey, Peter-One"
      quote="With great power, comes great responsibility"
      color="red"
      hoverColor="skyblue"
    />
  </section>
  <section id="deadpool">
    <CharSection
      heroId="deadpool"
      photo="deadpool-hero.png"
      width="45%"
      margin="0em"
      name="Deadpool"
      realName="Wade Wilson"
      about="Deadpool, aka Wade Wilson, is a former special forces operative turned mercenary who gained accelerated healing abilities after being subjected to an experimental regenerative mutation. With his newfound powers, he uses his dark humor, breaking-the-fourth-wall antics, and tendency to disregard conventional morality to fight against evil, often in his own unorthodox and violent way. Despite his rough exterior, Deadpool has a soft spot for those in need and has become a fan favorite for his irreverent and unconventional approach to superheroism."
      origin="Unrevealed location in Canada"
      alias="Merc with a Mouth"
      hoverColor="darkred"
    />
  </section>
</template>

<style scoped>
header {
  line-height: 1.5;
  position: sticky;
  z-index: 100;
  top: 18px;

  margin-bottom: 2em;

  display: flex;
  justify-content: center;
  align-items: center;
}

@media (max-width: 800px) {
  header {
    display: none;
  }
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

  scroll-snap-align: start;
  scroll-margin-top: 100px;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
