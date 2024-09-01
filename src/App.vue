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
  <section id="iron">
    <CharSection
      photo="iron-man.png"
      name="Iron Man"
      about="Iron Man, aka Tony Stark, is a founding member of the Avengers and one of the most iconic characters in the Marvel universe. A billionaire inventor and philanthropist, Tony Stark created the Iron Man suit to save his own life and later used it to fight crime and protect the world from various threats. With his wit, intelligence, and advanced technology, Iron Man has become a beloved and respected superhero, known for his sarcastic humor and unwavering commitment to justice."
    />
  </section>
  <section>
    <CharSection
      photo="captain-hero.png"
      name="Captain America"
      about="Captain America, aka Steve Rogers, is a patriotic superhero and one of the most respected members of the Avengers. Created during World War II as part of a secret government experiment, Steve Rogers was transformed into a super-soldier with enhanced strength, agility, and endurance. With his indestructible shield and unwavering commitment to justice, Captain America has fought against tyranny and oppression, becoming a symbol of hope and freedom for generations of Americans. His strong moral compass and old-fashioned values have earned him the respect and admiration of his fellow Avengers and the public alike."
    />
  </section>
  <section>
    <CharSection
      photo="thor-hero.png"
      name="Thor"
      about="Thor is the Norse god of thunder and a founding member of the Avengers. With his incredible strength, lightning powers, and indestructible hammer Mjolnir, Thor has become a powerful force for justice and protection in the Marvel universe. As the son of Odin, the king of Asgard, Thor has a deep sense of duty and responsibility, but his arrogance and impulsiveness have also led to conflicts with his fellow Avengers. Despite this, Thor's bravery, loyalty, and sense of humor have made him a beloved and integral member of the team."
    />
  </section>
  <section>
    <CharSection
      photo="strange-hero.png"
      name="Doctor Strange"
      about="Doctor Strange, aka Stephen Strange, is a sorcerer and a master of the mystic arts. Once a brilliant and arrogant neurosurgeon, Strange's life was forever changed when a car accident left his hands crippled. Desperate to regain the use of his hands, Strange sought out the Ancient One, a powerful sorcerer who taught him the mystic arts. With his newfound abilities, Strange became the Sorcerer Supreme, protecting the Earth from magical threats and other-dimensional entities."
    />
  </section>
  <section>
    <CharSection
      photo="hulk-hero.png"
      name="Hulk"
      about="The Hulk, aka Bruce Banner, is a brilliant scientist who, due to exposure to gamma radiation, transforms into a giant, green-skinned monster with incredible strength and durability whenever he becomes angry or experiences strong emotions. As the Hulk, he has clashed with the military, other superheroes, and even himself, as he struggles to maintain control over his alter ego. Despite his destructive tendencies, the Hulk has also been a valuable member of the Avengers, using his incredible powers to protect the world from threats too great for mortal men."
    />
  </section>
  <section>
    <CharSection
      photo="spiderman-hero.png"
      name="Spider-Man"
      about="Spider-Man, aka Peter Parker, is a teenage nerd-turned-superhero who gained incredible powers after being bitten by a radioactive spider. With his powers, he fights crime and battles supervillains in New York City, all while balancing his personal life and keeping his secret identity hidden from the world. With his quick wit, agility, and web-slinging abilities, Spider-Man has become a beloved and iconic superhero, known for his catchphrase 'With great power comes great responsibility.'"
    />
  </section>
  <section>
    <CharSection
      photo="deadpool-hero.png"
      name="Deadpool"
      about="Deadpool, aka Wade Wilson, is a former special forces operative turned mercenary who gained accelerated healing abilities after being subjected to an experimental regenerative mutation. With his newfound powers, he uses his dark humor, breaking-the-fourth-wall antics, and tendency to disregard conventional morality to fight against evil, often in his own unorthodox and violent way. Despite his rough exterior, Deadpool has a soft spot for those in need and has become a fan favorite for his irreverent and unconventional approach to superheroism."
    />
  </section>
</template>

<style scoped>
header {
  line-height: 1.5;
  position: sticky;
  top: 10px;

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
