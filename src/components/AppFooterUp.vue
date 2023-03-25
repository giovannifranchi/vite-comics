<script>
import ListComponent from './ListComponent.vue';
export default {
    name: 'AppFooterUp',
    components: {
        ListComponent,
    }, 
    data(){
        return {
            options: [
                {
                    title: 'dc comics',
                    listItems: [
                        'Characters',
                        'Comics',
                        'Movies',
                        'Tv',
                        'Games',
                        'Videos',
                        'News',
                    ]
                },
                {
                    title: 'dc',
                    listItems: [
                        'Terms of Use',
                        'Privacy Policy (new)',
                        'Ad Choices',
                        'Advertisings',
                        'Jobs',
                        'Subscriptions',
                        'Talent Workshops',
                        'CPSC Certificates',
                        'Ratings',
                        'Shop Help',
                        'Contact Us',
                    ]
                },
                {
                    title: 'sites',
                    listItems: [
                        'DC',
                        'MAD Magazine',
                        'DC Kids',
                        'DC Universe',
                        'DC Power Visa'
                    ]
                },
                {
                    title: 'shop',
                    listItems: [
                        'Shop DC',
                        'Shop DC Collectibles'
                    ]
                }
            ]
        }
    }
}
</script>

<template>
    <div class="wrapper">
        <div class="container">
            <ListComponent v-for="option in options" :title="option.title" :options="option.listItems" class="white"/>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;

.wrapper {
    @include jumbotron('../assets/img/footer-bg.jpg', center, round);
    .container{
        display: flex;
        height: 100%;
        padding: 50px 0;
        gap: 50px;
        @include container($container-big);
        background-image: url('../assets/img/dc-logo-bg.png');
        background-position: right;
        background-repeat: no-repeat;
        .white{
            color: #fff;
            :deep(li){
                margin: 10px 0;
                &:hover > a{
                    text-decoration: underline;
                }
            }
            :deep(h3){
                margin-bottom: 20px;
            }
        }
    }
}
</style>