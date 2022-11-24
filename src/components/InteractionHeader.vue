<script>
export default {
  name: "InteractionHeader",
};
</script>


<template>
  <div class="interactions-site d-flex">
    <a href="#" class="btn position-relative">
      <i class="fa-solid fa-cart-shopping"></i>
      <span class="position-absolute translate-middle badge rounded-pill">
        0
      </span>
    </a>
    <a href="#">
      <i class="fa-regular fa-circle-user"></i>
    </a>
    <div class="search">
      <input type="text" placeholder="Search ..." />
      <span>
        <i class="fa-solid fa-magnifying-glass"></i>
      </span>
    </div>
  </div>
</template>


<style lang="scss" scoped>
@use '../scss/partials/mixins' as *;
@use '../scss/partials/variables' as *;
    .interactions-site {
        @include centerFlex("vertical");
        a {
            color: #333333;
            font-size: 1.2rem;
            margin-left: 20px;
            &:first-of-type {
                margin: 0;
            }
            span {
                top: 5px;
                left: 80%;
                background-color: $secondary-color;
                font-size: 0.6rem;
            }
        }
    }
    .search {
        background-color: white;
        border-radius: 5px;
        padding: 10px 25px;
        margin-left: 20px;
        width: 180px;
        input {
            background-color: white;
            border: none;
            width: 80%;
            &:focus {
                outline: none;
            }
        }
        span i {
            color: $secondary-color;
            cursor: pointer;
        }
    }
</style>