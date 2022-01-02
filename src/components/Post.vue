<template>
  <a href="#" class="post">
    <div
      class="post_img"
      :style="{
        backgroundImage: `url(${require(`../assets/${img}.png`)})`,
        backgroundSize: 'cover',
      }"
    ></div>
    <div class="post_content">
      <h3 class="post_title">{{ title }}</h3>
      <div>
        <small class="post_label">{{ genre }}</small>
        <div class="post_author">{{ author }}</div>
      </div>
    </div>
  </a>
</template>

<script>
export default {
  name: "Post",
  props: {
    img: String,
    title: String,
    genre: String,
    author: String,
  },
};
</script>

<style scoped>
.post {
  width: 320px;
  height: 350px;
  background-color: #000000;
  margin-bottom: 2em;
  margin-right: 2em;
  position: relative;
  color: #ffffff;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  text-transform: uppercase;
  overflow: hidden;
}

.post_content {
  position: relative;
  z-index: 4;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 0.5em 1em;
}

.post_img {
  z-index: 2;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.post_title {
  font-size: 1.4rem;
  letter-spacing: 10px;
  font-weight: 500;
}

.post_label {
  font-size: 12px;
  font-weight: 300;
  letter-spacing: 4px;
}

.post_author {
  font-size: 0.9rem;
  font-weight: 400;
  letter-spacing: 6px;
  line-height: 2rem;
}
</style>
