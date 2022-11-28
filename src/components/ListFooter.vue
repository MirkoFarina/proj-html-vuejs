<script>
export default {
    name: 'ListFooter',
    props: {
        listItem: Object
    }
}
</script>

<template>
    <h5>
        {{listItem.name}}
    </h5>
    <ul>
        <li v-for="(item, index) in listItem.listItem" :key="index">
            <a :href="item.href">
                {{item.name}}
            </a>
        </li>
    </ul>
</template>



<style lang="scss" scoped>
@use '../scss/partials/variables' as *;
h5 {
    text-transform: capitalize;
    font-weight: 700;
}
ul {
    padding: 0;
    list-style: none;
    li {
        margin-bottom: 20px;
        a {
            color: darken($text-color, 20%);
            font-size: .8rem;
            font-weight: 600;
            text-transform: capitalize;
        }
    }
}
</style>