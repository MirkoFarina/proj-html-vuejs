<script>
export default {
    name: 'QuestionLeft'
}
</script>


<template>
<div class="container">
    <div class="row">
        <div class="col-12 col-lg-4">
            <div class="title mb-5">
                <h6 class="mb-4">
                    WHY HESITATE TO REGISTER?
                </h6>
                <h2>
                    LEARN at you own <span>pace</span>
                </h2>
            </div>
            <ul>
                <li>
                    <a href="#">
                        Select & customize courses to your preferences
                    </a>
                </li>
                <li>
                    <a href="#">
                        Change the tutor and make arrangements
                    </a>
                </li>
                <li>
                    <a href="#">
                       Partecipate in events to join others
                    </a>
                </li>
                <li>
                    <a href="#">
                        Get the desired certificate delivered at house
                    </a>
                </li>
            </ul>
            <button type="button" class="btn mf-button btn-lg">
                Get started for free
                <i class="fa-solid fa-arrow-right-long"></i>
            </button>
        </div>
        <div class="col-12 col-lg-8 text-center right">
            <img src="../assets/img/home-5-image-01.png" alt="">
        </div>
    </div>
</div>
</template>



<style lang="scss" scoped>
@use '../scss/partials/variables' as *;

    ul {
        list-style-type: '\2714';
        font-weight: 700;
        color: $secondary-color;
        padding: 0;
        li {
            padding-left: 20px;
            font-size: .9rem;
            margin-bottom: 20px;
            &:last-child {
                margin-bottom: 60px;
            }
            a {
                color: darken($text-color, 30%);
            }
        }
    }

    button {
        padding: 13px 30px;
    }

    .right {
        position: relative;
        z-index: 2;
        &::after {
            content: '';
            position: absolute;
            top: 120px;
            left: 50px;
            background-image: url('../assets/img/underlay-shape-grey.svg');
            background-size: 70% 450px;
            background-repeat: no-repeat;
            width: 100%;
            height: 100%;
            z-index: -1;
        }
        &::before {
            content: '';
            position: absolute;
            top: 100px;
            right: 100px;
            background-image: url('../assets/img/maxcoach-shape-05.png');
            background-repeat: no-repeat;
            background-position: right;
            width: 100%;
            height: 100%;
            z-index: -1;
        }
    }
</style>