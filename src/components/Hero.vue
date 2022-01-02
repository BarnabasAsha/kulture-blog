<template>
  <div class="hero">
    <div class="hero_block _left"></div>
    <div class="hero_container">
      <div class="hero_img">
        <img src="../assets/img-hero.png" alt="" />
      </div>
      <div class="hero_heading">
        <h1>
          nightlights- <br />
          Malibu,CA
        </h1>
        <p>An in-depth take of the party scene on the west coast</p>
      </div>
    </div>
    <div class="hero_block _right"></div>
  </div>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style scoped>
.hero {
  width: 100%;
  display: grid;
  grid-template-columns: 2fr 12fr 2fr;
}

.hero_container {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
}

.hero_img {
  width: 100%;
  height: 550px;
}

.hero_block {
  border: 0.5px solid #000000;
  border-bottom: none;
}

.hero_heading {
  position: relative;
  width: 500px;
  height: 200px;
  background: #000000;
  color: #ffffff;
  padding: 1em 1.5em;
  margin-right: 5em;
  margin-top: -120px;
}

.hero_heading h1 {
  display: block;
  width: 70%;
  font-size: 2rem;
  font-weight: 300;
  letter-spacing: 20px;
  text-transform: uppercase;
  margin-bottom: 1em;
}

.hero_heading p {
  font-weight: 300;
  font-size: 1rem;
  letter-spacing: 6px;
  line-height: 2rem;
  text-transform: uppercase;
}
</style>
