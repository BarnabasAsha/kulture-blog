<template>
  <div class="mobile_nav">
    <nav class="">
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
      <div class="mobile_nav_socials">
        <a href="#">TW</a>
        <a href="#">IG</a>
      </div>
    </nav>
  </div>
</template>
<script>
export default {
  name: "MobileNav",
};
</script>

<style scoped>
.mobile_nav {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background: #000000;
  color: #ffffff;
  z-index: 200;
}

.mobile_nav a {
  font-size: 0.9rem;
  letter-spacing: 12px;
  font-weight: 400;
}

.mobile_nav nav {
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  animation-name: slide;
  animation-duration: 2s;
}

.mobile_nav ul {
  padding: 0;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.mobile_nav ul li {
  margin: 15px 0;
}

.mobile_nav_socials {
  width: 100%;
  align-items: center;
  display: flex;
  justify-content: center;
}

.mobile_nav_socials a {
  border: 1px solid #fff;
  padding: 0.5em;
  /* margin-right: 5px; */
}

@keyframes slide {
  from {
    opacity: 0;
    transform: translateY(80px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media screen and (min-width: 801px) {
  .mobile_nav {
    display: none;
  }
}
</style>
