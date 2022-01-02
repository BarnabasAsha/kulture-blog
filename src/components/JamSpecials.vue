<template>
  <div class="jam_specials">
    <div class="jam_specials_container">
      <h2>JAM SPECIALS</h2>
      <p>our takes on the latest hits on the airwaves</p>
      <div class="jam_specials_row"></div>
    </div>
    <div class="jam_specials_block"></div>
  </div>
</template>

<script>
export default {
  name: "JamSpecials",
};
</script>

<style scoped>
.jam_specials {
  position: relative;
  width: 100%;
  display: grid;
  grid-template-columns: 14fr 2fr;
}

.jam_specials_block {
  background: #ffffff;
  width: 100%;
  border: 0.5px solid #000000;
  border-top: none;
  box-sizing: border-box;
}

.jam_specials_container {
  padding-left: 15%;
  padding-top: 1em;
  background: #000000;
  color: #ffffff;
  height: 500px;
  text-transform: uppercase;
}

.jam_specials_container h2 {
  line-height: 48px;
  font-weight: bold;
  font-size: 2rem;
  letter-spacing: 24px;
}

.jam_specials_container p {
  font-size: 1rem;
  letter-spacing: 12px;
  font-weight: 300s;
}
</style>
