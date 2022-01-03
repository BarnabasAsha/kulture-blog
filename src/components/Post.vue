<template>
  <a href="#" class="post">
    <div class="post_content">
      <h3 class="post_title">{{ title }}</h3>
      <div>
        <small class="post_label">{{ genre }}</small>
        <div class="post_author">{{ author }}</div>
      </div>
    </div>
    <div
      class="post_img"
      :style="{
        backgroundImage: `url(${require(`../assets/${img}.png`)})`,
        backgroundSize: 'cover',
      }"
    ></div>
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
  min-width: 350px;
  width: 350px;
  height: 400px;
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
  padding: 1em;
}

.post_content:hover + .post_img {
  transform: scale(1.1);
}

.post_img {
  z-index: 2;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  transition: all ease-in-out 0.7s;
}

.post_title {
  font-size: 1.4rem;
  line-height: 2.4rem;
  letter-spacing: 12px;
  font-weight: 500;
  margin-top: 0;
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
  line-height: 1rem;
  margin-top: 8px;
}

@media screen and (max-width: 800px) {
  .post {
    min-width: 250px;
    width: 250px;
    height: 320px;
  }
}

@media screen and (max-width: 500px) {
  .post {
    min-width: 230px;
    width: 230px;
    height: 300px;
  }

  .post_title {
    font-size: 1.2rem;
    letter-spacing: 8px;
    font-weight: 500;
  }

  .post_label {
    font-size: 0.6rem;
  }

  .post_author {
    font-size: 0.8rem;
  }
}
</style>
