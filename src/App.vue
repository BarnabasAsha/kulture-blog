<template>
  <Header />
  <Hero />
  <div class="mid_block"></div>
  <Posts />
  <JamSpecials />
</template>

<script>
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import Posts from "./components/Posts.vue";
import JamSpecials from "./components/JamSpecials.vue";

export default {
  name: "App",
  components: {
    Header,
    Hero,
    Posts,
    JamSpecials,
  },
};
</script>

<style>
@import url("https://fonts.cdnfonts.com/css/space-grotesk");

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  padding: 0;
  font-family: "Space Grotesk", sans-serif;
  width: 100%;
  overflow-x: hidden !important;
}

a {
  text-decoration: none;
  color: inherit;
}

ul {
  list-style: none;
}

img {
  width: 100%;
  height: 100%;
}

.mid_block {
  height: 150px;
  border: 0.5px solid #000000;
}
</style>
