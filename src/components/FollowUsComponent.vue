<script>
import { stringifyExpression } from '@vue/compiler-core';

export default {
    name: 'FollowUsComponent',
    props: {
        title: String,
        icons: Array,
    }
}
</script>

<template>
    <div>
        <h3>{{ title }}</h3>
        <a href="#" v-for="icon in icons">
            <img :src="icon.iconSrc" :alt="icon.iconSocial">
        </a>
    </div>
</template>

<style lang="scss" scoped>
div {
    display: flex;
}
</style>