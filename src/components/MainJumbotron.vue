<script>
import ButtonComponent from './ButtonComponent.vue';
export default {
    name: 'Jumbotron',
    components: {
        ButtonComponent,
    },
    data(){
        return {
            buttonText: 'CURRENT SERIES',
        }
    }
}
</script>

<template>
    <div class="jumbo">
        <div class="container">
            <ButtonComponent class="btn" :text="buttonText"/>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;
.jumbo {
    height: 400px;
    @include jumbotron('../assets/img/jumbotron.jpg', center, no-repeat);
    .container{
        height: 100%;
        display: flex;
        @include container ($container-big);
        .btn {
            width: 250px;
            background-color: $primary-color;
            color: #fff;
            padding: 10px 0;
            align-self: flex-end;
            position: relative;
            top: 11%;
            transform: translateY(-50%);
            border: 0;
            font-size: 20px;
            font-weight: 600;
            cursor: pointer;
            &:hover {
                background-color: darken($primary-color, 5%);
            }
        }
    }
}
</style>