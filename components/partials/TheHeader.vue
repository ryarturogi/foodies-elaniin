<template>
  <header class="l-header">
    <div class="c-header">
      <TheLogo :dark-mode="darkMode" />
      <TheNavbar :dark-mode="darkMode" />
    </div>
  </header>
</template>

<script>
import TheLogo from "@/components/partials/TheLogo";
import TheNavbar from "@/components/partials/TheNavbar";
export default {
  components: {
    TheLogo,
    TheNavbar,
  },
  props: {
    darkMode: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {
      title: "Foodies",
    };
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/abstracts/variables.scss";
@import "@/assets/scss/base/breakpoints.scss";

.l-header {
  width: 100vw;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  flex-direction: column;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 2;
}
.c-header {
  width: 100%;
  height: 10.4rem;
  max-width: $screen-xl-min;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: relative;

  @include l {
    justify-content: flex-start;
    height: 12.4rem;
  }
}
</style>
