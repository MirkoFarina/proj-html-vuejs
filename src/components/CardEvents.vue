<script>
export default {
    name: 'CardEvents',
    props: {
        cards: Object
    }
}
</script>

<template>
<div v-for="(card, index) in cards" :key="index" class="col mb-3">
    <div class="mf-card d-flex">
        <div class="left">
            <div class="location">
                <i class="fa-solid fa-location-dot mx-2"></i>
                <span>
                    {{card.place}}
                </span>
            </div>
            <div class="title">
                <h3>
                    {{card.name}}
                </h3>
            </div>
        </div>

        <div class="right text-center">
            <div class="day">
                <span>
                    {{card.day}}
                </span>
                <p>
                    {{card.month}}
                </p>
            </div>
            <div>
                <button type="button" class="btn mf-button btn-lg">
                    Get ticket
                </button>
            </div>
        </div>
    </div>
</div>
</template>



<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
.mf-card {
    justify-content: space-between;
    background-color: lighten($background-color, 5%);
    border-radius: 5px;
    padding: 20px;
    &:hover {
        box-shadow: inset 7px 0px 0px -3px $secondary-color;
        background-color: white;
    }
    .left {
        width: 70%;
        .location {
            color: $text-color;
            font-size: .8rem;
            margin-bottom: 15px;
        }
        .title {
            text-transform: capitalize;
        }
    }
    .right {
        width: 30%;
        span {
            font-size: 2.8rem;
            color: $secondary-color;
        }
        p {
            text-transform: uppercase;
            font-weight: 700;
        }
    }
}
</style>