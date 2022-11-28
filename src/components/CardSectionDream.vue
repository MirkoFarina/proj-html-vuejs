<script>
export default {
    name:'CardSectionDream',
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
    <div class="mf-card col">
       <div class="img-top text-center">
            <img :src="getImagePath(card.pathImg)" :alt="card.name">
       </div>
        <div class="card-body text-center">
            <h5>{{card.name}}</h5>
            <p class="card-text">{{card.overview}}</p>
            <a :href="card.id" class="btn">Start now <span><i class="fa-solid fa-arrow-right-long"></i></span></a>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
    .mf-card {
        .img-top {
            margin-bottom: 30px;
        }
        h5 {
            color: $black-color;
            font-weight: 700;
        }
        p {
            color: lighten($black-color, 20%);
            font-size: .9rem;
        }
        a {
            color: lighten($primary-color, 30%);
            font-weight: 700;
            font-size: .8rem;
            &:hover {
                color: #20ad96;
            }
            span {
                display: inline-block;
                padding-left: 20px;
            }
        }
    }
        
</style>