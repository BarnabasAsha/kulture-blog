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
        <a href="#">TW</a>
        <a href="#">IG</a>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
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
  display: flex;
  justify-content: space-around;
  align-items: center;
}
</style>
