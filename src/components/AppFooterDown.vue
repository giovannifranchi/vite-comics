<script>
import ButtonComponent from './ButtonComponent.vue';
import FollowUsComponent from './FollowUsComponent.vue';
export default {
    name: 'AppFooterDown',
    components: {
        ButtonComponent,
        FollowUsComponent,
    },
    data(){
        return {
            buttonText: 'SIGN UP NOW',
            followText: 'FOLLOW US',
            icons: [
                {
                    social: 'Facebook',
                    iconSrc: 'src/assets/img/footer-facebook.png',
                }, 
                {
                    social: 'Twitter',
                    iconSrc: 'src/assets/img/footer-twitter.png',
                }, 
                {
                    social: 'YouTube',
                    iconSrc: 'src/assets/img/footer-youtube.png',
                }, 
                {
                    social: 'Pinterest',
                    iconSrc: 'src/assets/img/footer-pinterest.png',
                }, 
                {
                    social: 'Periscope',
                    iconSrc: 'src/assets/img/footer-periscope.png',
                }, 
            ]
        }
    }
}
</script>

<template>
<div class="wrapper">
    <div class="container">
        <ButtonComponent  class="btn" :text="buttonText"/>
        <FollowUsComponent :title="followText"
        :icons="icons"
        class="social"
        />
    </div>
</div>
</template>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;

.wrapper {
    background-color: $tertiary-color;
}

.container {
    @include container($container-big);
    display: flex;
    justify-content: space-between;
    padding: 30px 0;
    .btn {
        color: #fff;
        background-color: transparent;
        border: 1px solid $primary-color;
        width: auto;
        padding: 20px;
        cursor: pointer;
        &:hover {
            opacity: 0.7;
        }
    }
    .social {
        align-items: center;
        :deep(h3){
            color: $primary-color;
            padding-right: 50px;
        }
        :deep(a){
            padding: 0 5px;
            &:hover {
                opacity: 0.7;
            }
        }
    }
}
</style>