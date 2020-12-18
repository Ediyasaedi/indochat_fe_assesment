<template>
  <ul class="menu">
    <div
      class="menu-indicator"
      :style="{ left: positionToMove, width: sliderWidth }"
    ></div>
    <li
      class="menu-item"
      v-for="link in links"
      :key="link.id"
      @click="sliderIndicator(link.id)"
      :ref="'menu-item_' + link.id"
    >
      <a
        href="#"
        class="menu-link"
        :class="link.id === selectedIndex ? 'active' : null"
      >
        <strong>{{ link.text }}</strong>
      </a>
    </li>
  </ul>
</template>

<script>
export default {
  name: "DiscoverNavbar",
  data() {
    return {
      sliderPosition: 0,
      selectedElementWidth: 0,
      selectedIndex: 0,
      links: [
        {
          id: 1,
          text: "Discover A",
          img: "../assets/discover_a.png",
          content:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. In aliquid et illo iure nemo, omnis, impedit provident eum alias obcaecati amet labore quisquam dicta suscipit quod ipsum tempora iusto eos.",
        },
        {
          id: 2,
          text: "Discover B",
          img: "../assets/discover_b.png",
          content:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. In aliquid et illo iure nemo, omnis, impedit provident eum alias obcaecati amet labore quisquam dicta suscipit quod ipsum tempora iusto eos.",
        },
        {
          id: 3,
          text: "Discover C",
          img: "../assets/discover_c.png",
          content:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. In aliquid et illo iure nemo, omnis, impedit provident eum alias obcaecati amet labore quisquam dicta suscipit quod ipsum tempora iusto eos.",
        },
        {
          id: 4,
          text: "Discover D",
          img: "../assets/discover_d.png",
          content:
            "Lorem ipsum dolor, sit amet consectetur adipisicing elit. In aliquid et illo iure nemo, omnis, impedit provident eum alias obcaecati amet labore quisquam dicta suscipit quod ipsum tempora iusto eos.",
        },
      ],
    };
  },
  methods: {
    sliderIndicator(id) {
      let el = this.$refs[`menu-item_${id}`][0];
      this.sliderPosition = el.offsetLeft;
      this.selectedElementWidth = el.offsetWidth;
      this.selectedIndex = id;
    },
  },
  computed: {
    positionToMove() {
      return this.sliderPosition + "px";
    },
    sliderWidth() {
      return this.selectedElementWidth + "px";
    },
  },
};
</script>

<style lang="scss">
:root {
  --active-color: #f0f0f0;
  --link-text-color: #4b4b4b;
  --menu-background-color: #f7f7f7;
  --active-background-color: #5093f8;
}
/* ul */
.menu {
  padding: 0;
  margin: 0;
  position: relative;
  background-color: var(--menu-background-color);
  display: inline-flex;
  border-radius: 4px;
  list-style-type: none;
  overflow: hidden;
  &-item {
    display: inline-flex;
  }
  &-link {
    padding: 0.75rem 1rem;
    display: inline-flex;
    align-items: center;
    color: var(--link-text-color);
    text-decoration: none;
    &:hover,
    &.active {
      color: var(--active-color);
      background-color: var(--active-background-color);
    }
  }
  &-indicator {
    position: absolute;
    height: 0.25rem;
    background-color: var(--active-color);
    bottom: 0;
    left: 0;
    margin: auto;
    width: 3rem;
    transition: all ease 0.5s;
  }
}
</style>
