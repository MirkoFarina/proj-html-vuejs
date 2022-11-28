<script>
import { navHeaderData } from "../data/allDataSection";
import NavbarHeader from "./NavbarHeader.vue";
import InteractionHeader from "./InteractionHeader.vue";
export default {
  name: "HamburgerHeader",
  components: {
    NavbarHeader,
    InteractionHeader,
  },
  data() {
    return {
      navHeaderData,
      isOpen: false,
    };
  },
};
</script>


<template>
  <div class="hamburger d-block d-lg-none">
    <i @click="isOpen = !isOpen" class="fa-solid fa-bars"></i>
    <div v-if="isOpen" class="content-hamburger d-flex">
      <NavbarHeader
        @click="isOpen = !isOpen"
        class="d-block"
        :dataHeader="navHeaderData"
      />
      <InteractionHeader />
    </div>
  </div>
</template>



<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
.hamburger {
  i {
    font-size: 2rem;
    color: $primary-color;
  }
  .content-hamburger {
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0;
    z-index: 899;
    background-color: white;
    flex-direction: column;
    justify-content: space-between;
  }
}
</style>