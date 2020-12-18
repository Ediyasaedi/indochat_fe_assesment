<template>
  <div>
    <Navbar />
    <Home />
    <Discover />
    <GetInTouch />
  </div>
</template>

<script>
import Home from "./components/Home.vue";
import Navbar from "./components/Navbar.vue";
import Discover from "./components/Discover.vue";
import GetInTouch from "./components/GetInTouch.vue";

export default {
  name: "App",
  components: {
    Home,
    Navbar,
    Discover,
    GetInTouch,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
