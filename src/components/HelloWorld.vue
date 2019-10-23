<template>
  <div id="app"></div>
</template>

<script>
import "particles.js";

export default {
  name: "VueParticleJs",

  props: {
    config: Object,
    domId: String
  },
  mounted() {
    if (typeof this.domId !== "string") throw new Error("Invalid Dom object Provided");
    window.particlesJS(this.domId, { ...this.config }, function() {
      // eslint-disable-next-line no-console
      console.log("callback - particles.js config loaded");
    });
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
/* #particles-js {
  width: 100%;
  height: 100%;
  background-color: #b61924;
  background-image: url("");
  background-size: cover;
  background-position: 50% 50%;
  background-repeat: no-repeat;
} */
</style>
