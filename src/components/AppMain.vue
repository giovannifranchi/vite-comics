<script>
import MainJumbotron from './MainJumbotron.vue';
import MainList from './MainList.vue';
export default {
    name: 'AppMain',
    components: {
        MainJumbotron,
        MainList,
    }
}
</script>

<template>
    <MainJumbotron/>
    <MainList/>
</template>

<style lang="scss" scoped>
</style>