<script>
import { dataFooterAddress, dataSocial, dataFooterExploreL, dataFooterExploreR, dataFooterInformation } from '../data/dataFooter';
import ListFooter from './ListFooter.vue';
import ListFooterSocial from './ListFooterSocial.vue';
  export default {
    name: 'FooterApp',
    components: {
        ListFooter,
        ListFooterSocial
    },
    data(){
      return {
        dataFooterAddress,
        dataSocial,
        dataFooterExploreL,
        dataFooterExploreR,
        dataFooterInformation
      }
    }
  }
</script>

<template>
<footer>
    <div class="container">
        <div class="row">
            <div class="col-6">
                <ListFooter :listItem="dataFooterAddress"/>
                <ListFooterSocial :listItem="dataSocial" />
            </div>
            <div class="col-4 d-flex justify-content-between">
                <div class="left d-flex">
                    <div class="first-col">
                        <ListFooter :listItem="dataFooterExploreL"/>
                    </div>
                    <div class="second-col">
                        <ListFooter :listItem="dataFooterExploreR"/>
                    </div>
                </div>
                <div class="right">
                    <ListFooter :listItem="dataFooterInformation"/>
                </div>
            </div>
        </div>
    </div>
    <div class="text-center footer-bottom">
        <span>
            &#169; 2020 Maxcoach. All Rights Reserved
        </span>
        <div class="text-end">
            <a href="#" class="btn mf-button btn-lg">
                <i class="fa-solid fa-arrow-up-long"></i>
            </a>
        </div>
    </div>
</footer>
</template>


<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
.left {
    .first-col {
        margin-right: 50px;
    }
    .second-col {
        padding-top: 24px;
    }
}

.footer-bottom {
    padding: 50px;
    span {
        font-size: .8rem;
        color: $text-color;
    }
    a {
        border-radius: 50%;
    }
}
</style>