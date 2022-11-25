<script>
export default {
    name: 'StaticsApp',
    props: {
        statics: Array
    }
}
</script>

<template>
    <div class="statics">
        <div class="container all-statics">
            <div v-for="(item, index) in statics" :key="index" class="content text-center">
                <h4>
                    {{item.number}}
                </h4>
                <span>
                    {{item.name}}
                </span>
            </div>
        </div>
    </div>
</template>



<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
@use '../scss/partials/mixins' as *;
.statics {
    background-color:lighten($background-color, 5%);
    padding: 70px 0 ;
    .all-statics {
        display: flex;
        flex-wrap: wrap;
        @include justifyContents($type: 'around')
    }
    h4 {
        color: $secondary-color;
        font-size: 3rem;
        font-weight: 700;
    }
    span {
        text-transform: uppercase;
        font-weight: 700;
    }
}
</style>