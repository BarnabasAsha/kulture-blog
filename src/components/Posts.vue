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
        <Post
          v-for="post in postData"
          :key="post.title"
          :title="post.title"
          :img="post.img"
          :genre="post.genre"
          :author="post.author"
        />
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
  width: 100%;
  position: relative;
  margin-top: -260px;
  width: 100%;
  display: grid;
  grid-template-columns: 2fr 12fr 2fr;
  overflow-x: hidden;
}

.posts_block {
  border: 0.5px solid #000000;
  border-bottom: none;
  border-top: none;
}

.posts_heading {
  position: relative;
  width: 250px;
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
  right: 20px;
  bottom: 25px;
  width: 20px;
}

.posts_heading h2 {
  font-size: 2rem;
  letter-spacing: 16px;
  font-weight: 500;
}

.posts_container {
  padding: 50px 0;
  height: 670px;
}

.posts_roll {
  width: 100%;
  position: absolute;
  top: 200px;
  left: 12.5%;
  display: flex;
  margin-top: 1.8em;
  overflow-x: scroll;
  -ms-overflow-style: none; /* IE and Edge */
  scrollbar-width: none; /* Firefox */
}

.posts_roll::-webkit-scrollbar {
  display: none;
}

@media screen and (max-width: 800px) {
  .posts_container {
    height: auto;
  }
  .posts_roll {
    top: 0;
    left: 0;
    /* margin-top: 0; */
    position: static;
    flex-wrap: wrap;
  }
}

@media screen and (max-width: 500px) {
  .posts {
    margin-top: -200px;
  }

  .posts_heading {
    height: 100px;
    width: 180px;
  }

  .posts_heading h2 {
    font-size: 1.5rem;
  }

  .posts_heading_svg {
    right: 12px;
    bottom: 12px;
    width: 15px;
  }
}
</style>
