<template>
  <div class="jam_special">
    <div
      class="jam_special_img"
      :style="{
        backgroundImage: `url(${require(`../assets/${img}.png`)})`,
        backgroundSize: 'cover',
      }"
    ></div>
    <div class="jam_special_title">
      <small>{{ artist }}</small>
      <h4>{{ title }}</h4>
    </div>
  </div>
</template>

<script>
export default {
  name: "JamSpecial",
  props: {
    img: String,
    title: String,
    artist: String,
  },
};
</script>

<style scoped>
.jam_special {
  min-width: 280px;
  width: 280px;
  height: 400px;
  margin-bottom: 2em;
  margin-right: 2em;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  text-transform: uppercase;
}

.jam_special_img {
  overflow: hidden;
  width: 100%;
  height: 80%;
  filter: drop-shadow(15px 15px 15px rgba(89, 31, 13, 0.15));
}

.jam_special_title small {
  font-size: 10px;
  font-weight: 300;
  letter-spacing: 2px;
}

.jam_special_title h4 {
  font-size: 1rem;
  line-height: 1rem;
  margin: 0;
  font-weight: 500;
  letter-spacing: 4px;
  margin-top: 5px;
}

@media screen and (max-width: 800px) {
  .jam_special {
    min-width: 230px;
    width: 230px;
    height: 300px;
  }
}

@media screen and (max-width: 500px) {
  .jam_special {
    min-width: 200px;
    width: 200px;
    height: 270px;
  }
}
</style>
