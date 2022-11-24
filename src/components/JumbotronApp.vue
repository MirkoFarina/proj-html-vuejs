<script>
  export default {
    name: 'JumbotronApp'
  }
</script>

<template>
    <div class="jumbotron">
        <div class="content-jumbotron container">
           <div class="row">
                <div class="col-5 text">
                    <h2>
                        Complete Your Dreams in JavaS Programming
                    </h2>
                    <p>
                        Learn any coding program in distance and for a reasonable free. You don't have to struggle alone, you've got our assistance and help.
                    </p>
                    <button type="button" class="btn  btn-lg">
                        <i class="fa-solid fa-download"></i>
                        Download free E-book
                    </button>
                </div>
                <div class="col-7 img">
                    <img src="../assets/img/home-5-hero-image.png" alt="Img HomeStudy">
                </div>
           </div>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use '../scss/partials/mixins' as *;
@use '../scss/partials/variables' as *;

.jumbotron {
    background-color: $background-color;
    height: 700px;
}
.content-jumbotron {
    height: 100%;
    align-items: flex-start;
    padding: 50px 0;
    h2 {
        color: $primary-color;
        font-size: 3rem;
        font-weight: 600;
        margin-bottom: 30px;
    }
    p {
        font-weight: 600;
        font-size: 1.2rem;
        color: lighten($primary-color, 35%);
        margin-bottom: 50px;
    }
    button {
        background-color: $secondary-color;
        color: white;
        padding: 13px 30px;
        font-size: 1rem;
        font-weight: 700;
    }
    .text {
        align-self: center;
    }
    .img {
        text-align: end;
    }
}
</style>