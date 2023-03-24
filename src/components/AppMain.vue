<script>
import MainJumbotron from './MainJumbotron.vue';
import MainList from './MainList.vue';
import MainBanner from './MainBanner.vue';
export default {
    name: 'AppMain',
    components: {
        MainJumbotron,
        MainList,
        MainBanner,
    }
}
</script>

<template>
    <MainJumbotron/>
    <MainList/>
    <MainBanner/>
</template>

<style lang="scss" scoped>
</style>