<template>
  <div class="posts">
    <div class="posts_block"></div>
    <div class="posts_container">
      <div class="posts_heading">
        <h2>NEW<br />POSTS</h2>
        <div class="posts_heading_svg">
          <img src="../assets/arrow_right.svg" alt="" />
        </div>
      </div>
      <div class="posts_roll">
        <div v-for="post in postData" :key="post.title" class="glide__slide">
          <Post
            :title="post.title"
            :img="post.img"
            :genre="post.genre"
            :author="post.author"
          />
        </div>
      </div>
    </div>
    <div class="posts_block"></div>
  </div>
</template>

<script>
import Post from "./Post.vue";
import { ref } from "vue";

export default {
  name: "Posts",
  components: {
    Post,
  },
  setup() {
    const postData = ref([
      {
        title: "the look around",
        genre: "fashion",
        author: "debron smart",
        img: "look",
      },
      {
        title: "long exposure",
        genre: "photography",
        author: "marcos alves",
        img: "exposure",
      },
      {
        title: "vibes in la",
        genre: "fashion",
        author: "rahul malviya",
        img: "vibes",
      },
      {
        title: "timing",
        genre: "photography",
        author: "thoma fulloway",
        img: "timing",
      },
    ]);
    return { postData };
  },
};
</script>

<style scoped>
.posts {
  position: relative;
  margin-top: -260px;
  width: 100%;
  display: grid;
  grid-template-columns: 2fr 12fr 2fr;
}

.posts_block {
  border: 0.5px solid #000000;
  border-bottom: none;
  border-top: none;
}

.posts_heading {
  position: relative;
  width: 220px;
  height: 140px;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 0.5px solid #000000;
  border-left: 0;
  background: #ffffff;
}

.posts_heading_svg {
  position: absolute;
  right: 33px;
  bottom: 28px;
  width: 18px;
}

.posts_heading h2 {
  font-size: 1.6rem;
  letter-spacing: 10px;
  font-weight: 400;
}

.posts_container {
  padding: 50px 0;
  height: 550px;
}

.posts_roll {
  width: 100%;
  position: absolute;
  top: 200px;
  left: 12.5%;
  display: flex;
  /* justify-content: flex-end; */
  margin-top: 1.8em;
}
</style>
