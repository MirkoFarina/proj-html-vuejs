<script>
    import HeaderApp from './components/HeaderApp.vue';
    import MainApp from './components/MainApp.vue';
    import FooterApp from './components/FooterApp.vue';
  export default {
    name: 'App',
    components: {
        HeaderApp,
        MainApp,
        FooterApp
    }
  }
</script>

<template>
    <HeaderApp />
    <MainApp />
    <FooterApp/>
</template>


<style lang="scss">
    @use './scss/general.scss';
    @use './scss/partials/variables' as *;
    .title {
        h6 {
            color: darken($text-color, 30%);
            text-transform: uppercase;
            span {
                font-weight: bold;
            }
        }
        h2 {
            color: $primary-color;
            text-transform: capitalize;
            font-size: 3rem;
            font-weight: 700;
        span {
            color: $secondary-color;
            font-weight: 400;
        }
        }
    }
</style>
