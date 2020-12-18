<template>
  <div>
    <div class="container">
      <img src="../assets/discover.png" alt="" />
      <h3>DISCOVER</h3>
      <span>BOOKED TOOL</span>
    </div>
    <DiscoverNavbar />
  </div>
</template>

<script>
import DiscoverNavbar from "./DiscoverNavbar.vue";

export default {
  name: "Discover",
  components: {
    DiscoverNavbar,
  },
};
</script>

<style scoped lang="scss">
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin-top: 40px;
  margin-bottom: 40px;
}
</style>
