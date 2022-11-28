<script>
export default {
    name: 'CardCourses',
    props: {
        content: Object
    },
    methods: {
        getImagePath(imageName){
            return new URL(`../assets/img/${imageName}`, import.meta.url).href
        }
    }
}
</script>


<template>
<div class="col">
    <div class="mf-card">
        <div class="top">
            <img :src="getImagePath(content.pathImg)" alt="foto course">
            <div class="price">
                <span>
                    {{content.price}}
                </span>
            </div>
        </div>
        <div class="bottom">
            <div class="operator">
                <img :src="getImagePath(content.profileImg)" alt="foto profilo">
                <span>
                    {{content.teacher}}
                </span>
            </div>
            <div class="description">
                <p>
                    {{content.title}}
                </p>
            </div>
            <div class="info d-flex">
                <div>
                    <span>
                        <i class="fa-regular fa-file-lines"></i>
                        {{content.lessons}} lessons
                    </span>
                </div>
                <div>
                    <span>
                        <i class="fa-regular fa-user"></i>
                        {{content.students}} students
                    </span>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
span {
    font-size: .8rem;
    color: gray;
    text-transform: capitalize;
    font-weight: 600;
}
.mf-card {
    margin-bottom: 30px;
    cursor: pointer;
    &:hover {
        box-shadow: 10px 10px 10px -10px rgba(0,0,0,0.10);
        .bottom {
            background-color: white;
        }
    }
    .top {
        margin-bottom: 25px; 
        position: relative;
        img {
            border-top-left-radius: 5px;
            border-top-right-radius: 5px;
        }
        .price {
            position: absolute;
            top: 0;
            right: 0;
            padding: 10px 20px;
            background-color: $secondary-color;
            border-top-right-radius: 5px;
            border-bottom-left-radius: 5px;
            span {
                color: white;
                font-size: 1.2rem
            }
        }
    }
    .bottom {
        padding: 0 35px;
        .operator {
            margin-bottom: 25px;
            img {
                border-radius: 50%;
                width: 30px;
            }
            span {
                margin-left: 20px;  
            }
        }
        .description {
            font-size: 1.3rem;
            font-weight: 700;
            text-transform: capitalize;
        }
        .info {
            span {
                &:first-child {
                    margin-right: 20px;
                }
            }
        }
    }
}
</style>