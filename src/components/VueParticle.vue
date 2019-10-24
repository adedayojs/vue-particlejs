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
    window.particlesJS(this.domId, {
      particles:this.config.particles,
      interactivity:this.config.interactivity,
      retina_detect:this.config.retina_detect
    }, function() {
      // eslint-disable-next-line no-console
      console.log("callback - particles.js config loaded");
    });
  }
};
</script>

<style>
</style>
