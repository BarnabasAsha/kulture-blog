<template>
  <header>
    <div class="header">
      <div class="header_logo" role="banner">
        KUL<br />
        TURE
      </div>
      <nav class="header_nav">
        <ul>
          <li>
            <a href="#">FASHION</a>
          </li>
          <li>
            <a href="#">LIFE</a>
          </li>
          <li>
            <a href="#">MUSIC</a>
          </li>
          <li>
            <a href="#">PHOTOS</a>
          </li>
        </ul>
      </nav>
      <div class="header_socials">
        <div class="header_socials_lang">
          <a href="#">TW</a>
          <a href="#">IG</a>
        </div>
        <button
          @click="() => (status = !status)"
          class="header_menu"
          :class="status ? '_active' : ''"
        >
          <span></span>
          <span></span>
          <span></span>
        </button>
      </div>
    </div>
  </header>
  <mobile-nav v-if="status" />
</template>

<script>
import MobileNav from "../components/MobileNav.vue";
import { ref } from "vue";

export default {
  name: "Header",
  components: {
    MobileNav,
  },
  setup() {
    const status = ref(false);
    return { status };
  },
};
</script>

<style scoped>
.header {
  width: 100%;
  height: 100px;
  align-items: center;
  display: grid;
  grid-template-columns: 2fr 12fr 2fr;
}

.header a {
  font-size: 0.9rem;
  letter-spacing: 12px;
  font-weight: 400;
}

.header_logo {
  width: 100%;
  height: 100%;
  font-size: 0.9rem;
  letter-spacing: 1rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.header_nav {
  width: 100%;
  height: 100%;
  border: 0.5px solid #000000;
  display: flex;
  justify-content: center;
  align-items: center;
}

.header_nav ul {
  display: flex;
}

.header_nav ul li {
  margin: 0 15px;
}

.header_socials {
  width: 100%;
  height: 100%;
}

.header_socials_lang {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.header_menu span {
  width: 25px;
  height: 1.5px;
  margin-bottom: 5px;
  background: #000000;
}

.header_menu {
  display: none;
}

@media screen and (max-width: 800px) {
  .header {
    height: 80px;
  }

  .header_nav {
    border-top: 0;
  }

  .header_nav ul {
    display: none;
  }

  .header_socials_lang {
    display: none;
  }

  .header_logo {
    padding: 5px;
    font-size: 0.5rem;
    letter-spacing: 3px;
  }

  .header_menu {
    z-index: 250;
    position: relative;
    border: none;
    background: none;
    outline: none;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .header_menu span {
    transition: all ease-in-out 0.5s;
  }

  .header_menu._active span {
    background: white;
  }

  .header_menu._active span:nth-child(1) {
    transform: rotate(45deg);
  }

  .header_menu._active span:nth-child(2) {
    transform: rotate(-45deg);
  }

  .header_menu._active span:nth-child(3) {
    display: none;
  }
}
</style>
