<script>
import AppLogo from './AppLogo.vue';
import HeaderList from './HeaderList.vue';
export default {
    name: 'Header',
    components: {
        AppLogo,
        HeaderList,
    },
}
</script>

<template>
    <header>
        <div class="container">
            <AppLogo class="logo"/>
            <HeaderList/>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
@use '../assets/style/partials/mixins' as *;



.container {
    @include container($container-big);
    display: flex;
    justify-content: space-between;
    padding: 10px 0;
    .logo {
        width: 75px;
    }
}

</style>