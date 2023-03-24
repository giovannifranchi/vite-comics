<script>
export default {
    name: 'BannerItems',
    props: {
        text: String,
        icon: String,
    }
}
</script>

<template>
    <div>
        <img :src="icon" :alt="text">
        <h5>{{ text }}</h5>
    </div>
</template>

<style lang="scss" scoped>
div{
    display: flex;
    align-items: center;
    gap: 10px;
}
</style>