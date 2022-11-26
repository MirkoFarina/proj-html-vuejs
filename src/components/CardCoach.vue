<script>
export default {
    name:'CardCoach',
    props: {
        card: Object
    },
    methods: {
        getImagePath(imageName){
            return new URL(`../assets/img/${imageName}`, import.meta.url).href
        }
    }
}
</script>

<template>
    <div class="mf-card text-center">
        <div class="content-card">
            <div class="top">
            <img :src="getImagePath(card.img)" alt="">
        </div>
        <div class="body">
            <p>
                {{card.description}}
            </p>
            <h5>
               {{card.name}}
            </h5>
            <span>
                / {{card.work}}
            </span>
        </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
.mf-card {
    background-color: white;
    box-shadow: 1px 8px 16px 3px rgba(0,0,0,0.1);
    border-radius: 5px;
    padding: 0 40px;
    padding-bottom: 30px;
    height: 400px;
    .content-card {
        margin-top: 100px;
    }
    img {
        border-radius: 50%;
        transform: translateY(-50%);
    }
    .body {
        transform: translateY(-30%);
        p {
           overflow: auto;
           color: $primary-color;
        }
        h5 {
            text-transform: uppercase;
        }
        span {
            text-transform: capitalize;
            color: $text-color;
            font-size: .7rem;
        }
    }
}
</style>