<script>
export default {
    name: 'ListFooterSocial',
    props:{
        listItem: Object
    }
}
</script>


<template>
    <ul>
        <li v-for="(item, index) in listItem.listItem" :key="index">
            <a href="#">
                <i class="fa-brands" :class="item.name"></i>
            </a>
        </li>
    </ul>
</template>

<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
ul {
    list-style: none;
    padding: 0;
    display: flex;
    li {
        padding-right: 30px;
    }
    a {
        color: $text-color;
        font-size: 1.5rem;
    }
}
</style>