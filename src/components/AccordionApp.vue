<script>
export default {
    name: 'accordion',
    props: {
        accordion: Array
    }
};
</script>

<template>
    <div class="mf-accordion">
        <div v-for="(accordionItem, index) in accordion" :key="index" class="mf-item">
            <div @click="accordionItem.isShow = !accordionItem.isShow"  class="header-accordion" :class="{'open' : accordionItem.isShow}">
                <h2>
                    {{accordionItem.title}}
                </h2>
                <span>
                    <i :class="{'d-none' : accordionItem.isShow}" class="fa-solid fa-circle-plus"></i>
                    <i :class="{'d-none' : !accordionItem.isShow}" class="fa-solid fa-circle-minus"></i>
                </span>
            </div>
            <div class="body-accordion " :class="{'no-show' : accordionItem.isShow}">
                <p>
                    {{accordionItem.body}}
                </p>
            </div>
        </div>
    </div>
</template>



<style lang="scss" scoped>
@use '../scss/partials/variables' as *;


.open {
    background-color: $secondary-color;
    color: white;
}



h2 {
    font-size: 1.3rem;
    font-weight: 700;
}
.mf-accordion  {
    .mf-item {
        box-shadow: 1px 8px 16px 3px rgba(0,0,0,0.1);
        margin-bottom: 40px;
        border-radius: 5px;
        color: lighten($black-color, 10%);
        position: relative;
        .header-accordion {
            position: relative;
            padding: 15px 40px 15px 15px;
            border-top-right-radius: 5px;
            border-top-left-radius: 5px;
            text-transform: capitalize;
            cursor: pointer;
            span {
                position: absolute;
                right: 15px;
                top: 50%;
                transform: translateY(-50%);
                i {
                    font-size: 1.5rem;
                }
            }
        }
        .no-show {
                max-height: 200px;
                overflow: auto;
            }
    }
    
}
.body-accordion {
            max-height: 0;
            transition: max-height .7s;
            overflow: hidden;
            p {
                padding: 20px;
            }
        }
</style>