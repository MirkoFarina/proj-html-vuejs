<script>
export default {
    name: 'QuestionRIght'
}
</script>


<template>
<div class="container">
    <div class="row">
        <div class="col-12 col-lg-7 text-center left mb-5">
            <img src="../assets/img/home-5-image-02.png" alt="">
            <div class="img-abs-left"></div>
            <div class="img-abs-right"></div>
        </div>
        <div class="col-12 col-lg-5 d-flex justify-content-center flex-column">
            <div class="title mb-5">
                <h6 class="mb-4 mt-5">
                   why are you looking for?
                </h6>
                <h2>
                   learn on your <span>mobile</span> anytime!
                </h2>
                <p>
                    Save lessons for later and revise or write ostes at any time and on multiple devices on your way. Never interfere with activities of anjoyment or other precious moments.
                </p>
            </div>
            
            <div>
                <button type="button" class="btn mf-button btn-lg">
                    Download our app
                </button>
            </div>
        </div>
    </div>
</div>
</template>



<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
    button {
        padding: 13px 30px;
    }

    .row {
        p {
            color: $text-color;
        }
    }

    .left {
        position: relative;
        z-index: 2;
        &::after {
            content: '';
            position: absolute;
            top: 80px;
            left: 20px;
            background-image: url('../assets/img/underlay-shape-grey.svg');
            background-size: 70% 500px;
            background-repeat: no-repeat;
            width: 100%;
            height: 100%;
            z-index: -1;
        }
        &::before {
            content: '';
            position: absolute;
            top: 100px;
            right: 90px;
            background-image: url('../assets/img/maxcoach-shape-07.png');
            background-repeat: no-repeat;
            background-position: right;
            width: 100%;
            height: 100%;
            z-index: -1;
        }
        .img-abs-left {
            position: absolute;
            top: 50%;
            left: -40px;
            width: 150px;
            height: 100px;
            background-image: url('../assets/img/maxcoach-shape-01.png');
            background-repeat: no-repeat;
        }
        .img-abs-right {
            position: absolute;
            top: 0;
            right: 50px;
            z-index: -1;
            &::after  {
                content: '';
                display: block;
                width: 70px;
                height: 70px;
                border-radius: 50%;
                border: 10px solid #ecc5ab;
                
            }
        }
    }
</style>