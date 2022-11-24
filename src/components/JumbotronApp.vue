<script>
  export default {
    name: 'JumbotronApp'
  }
</script>

<template>
    <div class="jumbotron">
        <div class="content-jumbotron container">
           <div class="row">
                <div class="col-12 col-lg-5 text">
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
                <div class="col-12 col-lg-7 img">
                    <img src="../assets/img/home-5-hero-image.png" alt="Img HomeStudy">
                </div>
           </div>
        </div>

        <div class="action-right">
            <nav>
                <ul>
                    <li>
                        <a href="#">
                            <i class="fa-solid fa-pen-ruler"></i>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <i class="fa-regular fa-life-ring"></i>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <i class="fa-solid fa-book"></i>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <i class="fa-solid fa-cart-shopping"></i>
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use '../scss/partials/mixins' as *;
@use '../scss/partials/variables' as *;

.jumbotron {
    background-color: $background-color;
    position: relative;
    &::before {
        content: '';
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        left:0;
        z-index: 0;
        background-image: url('../assets/img/jumbo-overlay.svg');
        background-size: 100% 420px;
        background-repeat: no-repeat;
        transform: scaleY(-1);
    }
}
.content-jumbotron {
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
    .col-12 {
        z-index: 1;
    }
}

.action-right {
    background-color: white;
    position: absolute;
    right: 0;
    top: 20%;
    transform: translateY(-50%);
    padding: 10px 10px;
    text-align: center;
    border-radius: 5px;
    box-shadow: -4px 3px 10px -5px gray;
    ul  {
    padding: 0;
    margin: 0;
    list-style: none;
    a {
        display: inline-block;
        color: black;
        margin-bottom: 10px;
    }
}
}
</style>