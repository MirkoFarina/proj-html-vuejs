<script>
import {navHeaderData} from '../data/allDataSection';
import NavbarHeader from "./NavbarHeader.vue";
import InteractionHeader from "./InteractionHeader.vue";
import HamburgerHeader  from "./HamburgerHeader.vue";
export default {
  name: "HeaderApp",
  components: {
    NavbarHeader,
    InteractionHeader,
    HamburgerHeader
  }, data(){
            return {
                navHeaderData,
                isOpen: false
            }
        }
};
</script>

<template>
  <header>
    <div class="container d-flex content-header">
      <div class="logo">
        <img src="/dark-logo.png" alt="Logo MaxCoach" />
      </div>

      <div class="right d-flex">
        <NavbarHeader class="d-none d-lg-flex" :dataHeader="navHeaderData"/>
        <InteractionHeader class="d-none d-lg-flex"/>
        <HamburgerHeader  class="d-lg-none d-flex" />
      </div>
    </div>
  </header>
</template>


<style lang="scss" scoped>
@use "../scss/partials/mixins" as *;
@use "../scss/partials/variables" as *;
header {
  background-color: $background-color;
  height: 100px;
  .content-header {
    height: 100%;
    @include centerFlex("vertical");
    @include justifyContents("between");
  }
  .logo img {
    width: 150px;
    vertical-align: middle;
  }
  .right {
    @include centerFlex("vertical");
  }
}
</style>