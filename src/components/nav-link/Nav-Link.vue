<template>
  <component
    :is="componentType"
    :to="to"
    class="dropdown-item"
    @click.stop="
      () => {
        scrollToElement(el);
        closeNav();
      }
    "
  >
    <slot></slot>
  </component>
</template>
<script>
export default {
  name: "nav-link",
  inject: ["closeNavbar", "closeDropDown"],
  props: {
    to: {
      type: [String, Object],
      default: undefined,
    },
    el: {
      type: [String, Object],
      default: undefined,
    },
  },
  computed: {
    componentType() {
      return this.to ? "router-link" : "a";
    },
  },
  methods: {
    scrollToElement(elementId) {
      const el = document.querySelector(elementId);
      if (el) {
        // Use el.scrollIntoView() to instantly scroll to the element
        el.scrollIntoView({ behavior: "smooth" });
      }
    },
    closeNav() {
      if (this.closeNavbar) {
        this.closeNavbar();
      }
      if (this.closeDropDown) {
        this.closeDropDown();
      }
    },
  },
};
</script>
<style lang="scss" scoped>
a {
  display: flex;
  align-items: baseline;
  color: #fff;
  text-decoration: none;
  text-transform: uppercase;
  font-size: 1rem;
  padding: 0.5rem 0.7rem;
  line-height: 1.625rem;
}
</style>
