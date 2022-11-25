<script>
import {navHeaderData} from '../data/allDataSection';
import NavbarHeader from "./NavbarHeader.vue";
import InteractionHeader from "./InteractionHeader.vue";
export default {
  name: "HeaderApp",
  components: {
    NavbarHeader,
    InteractionHeader,
  }, data(){
            return {
                navHeaderData
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
        <NavbarHeader :dataHeader="navHeaderData"/>
        <InteractionHeader />
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