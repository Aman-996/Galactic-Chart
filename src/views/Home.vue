<template>
  <div class="home">
    <solarSystem />
  </div>
</template>

<script>
// @ is an alias to /src
import solarSystem from "./solarSystem.vue";

export default {
  name: "home",
  components: {
    solarSystem,
  },
};
</script>
<style scoped>
.home {
  height: 100vh;
  width: 100vw;
}
</style>