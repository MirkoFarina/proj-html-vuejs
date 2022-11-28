<script>
import SliderCoach from './SliderCoach.vue';
export default {
    name: 'TemplateCoach',
    components: {
        SliderCoach
    },
    props: {
        dataCards: Array
    }
}
</script>

<template>
    <div class="container">
        <div class="title mb-5 text-center">
            <h6 class="mb-4 mt-5">
               people are praising maxcoach
            </h6>
            <h2>
                what make they  <span>love us?</span> 
            </h2>
        </div>
        <SliderCoach :arrayCards="dataCards" class="mb-5" />

        <div class="start-now">
            <div class="img-abs-right"></div>
            <div class="content-start d-flex">
                <h6>
                Start today for getting <span>Online Certification</span>
            </h6>
            <h4 class="mb-5">
                You can be you own guiding star with our help!
            </h4>
            <div>
                <button type="button" class="btn mf-button btn-lg">
                    Get started now
                </button>
            </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
.container {
    padding-top: 50px;
    .start-now {
        display: flex;
        align-items: center;
        justify-content: center;
        position: relative;
        padding-bottom: 80px;
        .content-start {
            width: 70%;
            background-color: #f6f6f6;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            position: relative;
            z-index:  5;
        }
        .img-abs-right {
            position: absolute;
            top: 20px;
            left: 50px;
            &::after  {
                content: '';
                display: block;
                width: 50px;
                height: 50px;
                border-radius: 50%;
                border: 6px solid #E6DCD2;
            }
        }
        &::after {
            content: '';
            position: absolute;
            top: 0px;
            right: 30px;
            background-image: url('../assets/img/maxcoach-shape-02.png');
            background-repeat: no-repeat;
            background-position: center;
            width: 150px;
            height: 150px;
            z-index: 0;
        }
        &::before {
            content: '';
            position: absolute;
            top: 90px;
            left: 50px;
            width: 150px;
            height: 40px;
            background-image: url('../assets/img/maxcoach-shape-01.png');
            background-repeat: no-repeat;
        }
        h6 {
            color: $primary-color;
            font-size: 1.8rem;
            span {
                color: $secondary-color;
            }
        }
        h4 {
            color: $primary-color;
            font-size: 2.4rem;
            font-weight: 700;
        }
        button {
            padding: 15px 60px;
        }
    }
}
</style>