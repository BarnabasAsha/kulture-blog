<template>
  <div class="jam_specials">
    <div class="jam_specials_container">
      <h2>JAM SPECIALS</h2>
      <p>our takes on the latest hits on the airwaves</p>
      <div class="jam_specials_row">
        <JamSpecial
          v-for="jam in jams"
          :key="jam.title"
          :title="jam.title"
          :img="jam.img"
          :artist="jam.artist"
        />
      </div>
    </div>
    <div class="jam_specials_block"></div>
  </div>
</template>

<script>
import { ref } from "vue";
import JamSpecial from "../components/JamSpecial.vue";

export default {
  name: "JamSpecials",
  components: {
    JamSpecial,
  },
  setup() {
    const jams = ref([
      {
        title: "gasolina",
        artist: "niqo nuevo",
        img: "gasolina",
      },
      {
        title: "gimme brain",
        artist: "travis barker ft. lil wayne & rick ross",
        img: "gimme",
      },
      {
        title: "pas ce soir",
        artist: "plk ft. krisky",
        img: "plk",
      },
      {
        title: "on my way!",
        artist: "snow tha product ft daddie juju",
        img: "omw",
      },
    ]);
    return { jams };
  },
};
</script>

<style scoped>
.jam_specials {
  position: relative;
  width: 100%;
  display: grid;
  grid-template-columns: 14fr 2fr;
  overflow-x: hidden;
}

.jam_specials_block {
  background: #ffffff;
  width: 100%;
  border: 0.5px solid #000000;
  border-top: none;
}

.jam_specials_container {
  padding-left: 15%;
  padding-top: 1em;
  background: #000000;
  color: #ffffff;
  height: 720px;
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
  line-height: 1.8rem;
  letter-spacing: 12px;
  font-weight: 300;
}

.jam_specials_row {
  width: 100%;
  position: absolute;
  top: 200px;
  left: 12%;
  display: flex;
  margin-top: 1em;
  overflow-x: scroll;
  -ms-overflow-style: none; /* IE and Edge */
  scrollbar-width: none; /* Firefox */
}

.jam_specials_row::-webkit-scrollbar {
  display: none;
}

@media screen and (max-width: 800px) {
  .jam_specials_container {
    height: auto;
  }

  .jam_specials_container h2 {
    letter-spacing: 16px;
  }

  .jam_specials_container p {
    letter-spacing: 8px;
  }

  .jam_specials_row {
    top: 0;
    left: 0;
    /* margin-top: 0; */
    position: static;
    flex-wrap: wrap;
  }
}
</style>
