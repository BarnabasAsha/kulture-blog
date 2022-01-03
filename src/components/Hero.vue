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
        <div class="hero_heading_svg">
          <img src="../assets/arrow_right_up.svg" alt="" />
        </div>
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
  position: relative;
  width: 100%;
  display: grid;
  grid-template-columns: 2fr 12fr 2fr;
}

.hero_container {
  position: relative;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  box-sizing: border-box;
}

.hero_img {
  width: 100%;
}

.hero_block {
  width: 100%;
  background: white;
  box-sizing: border-box;
  border: 0.5px solid #000000;
  border-bottom: none;
}

.hero_heading {
  position: relative;
  width: 600px;
  height: 240px;
  background: #000000;
  color: #ffffff;
  padding: 1em 1.5em;
  margin-right: 4%;
  margin-top: -120px;
}

.hero_heading h1 {
  display: block;
  width: 70%;
  font-size: 2rem;
  font-weight: 400;
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

.hero_heading_svg {
  position: absolute;
  right: 40px;
  top: 40px;
  width: 20px;
}

@media screen and (max-width: 800px) {
  .hero_heading {
    width: 70%;
    margin-right: 0;
  }

  .hero_heading h1 {
    font-size: 1.5rem;
    letter-spacing: 10px;
  }
}

@media screen and (max-width: 1030px) {
  .hero_heading {
    margin-right: 0;
  }
}

@media screen and (max-width: 500px) {
  .hero_img {
    height: 200px;
  }

  .hero_heading {
    width: 250px;
    height: 150px;
    margin-top: -80px;
  }

  .hero_heading_svg {
    position: absolute;
    right: 20px;
    top: 20px;
    width: 14px;
  }

  .hero_heading h1 {
    font-size: 1rem;
    letter-spacing: 5px;
  }

  .hero_heading p {
    font-size: 0.5rem;
    line-height: 1rem;
  }
}
</style>
