<script>
import dataHeader from '../data/navHeaderData';
    export default {
        name: 'NavbarHeader',
        data(){
            return {
                dataHeader
            }
        }
    }
</script>
<template>
    <ul>
        <li v-for="(link, index) in dataHeader" :key="index">
            <a :href="link.href">
                {{link.name}}
                <i v-if="!link.current" class="fa-solid fa-angle-down"></i>
                <i v-else class="fa-solid fa-angle-up"></i>
            </a>
        </li>
    </ul>
</template>


<style lang="scss" scoped>
    @use '../scss/partials/variables' as *;
    ul {
        list-style: none;
        display: flex;
        margin: 0;
        li {
            margin-left: 35px;
            &:first-child {
                margin-left: 0;
            }
        }
       a {
        color: $primary-color;
       }
       i {
        font-size: .7rem;
       }
    }
</style>