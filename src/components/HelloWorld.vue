<template>
<div></div>
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
</style>
