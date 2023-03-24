<script>
import BannerItems from './BannerItems.vue';
export default {
    name: 'MainBanner',
    components: {
        BannerItems,
    },
    data(){
        return {
            items: [
                {
                    icon: 'src/assets/img/buy-comics-digital-comics.png',
                    text: 'digital comics',
                },
                {
                    icon: 'src/assets/img/buy-comics-merchandise.png',
                    text: 'dc mercendise',
                },
                {
                    icon: 'src/assets/img/buy-comics-subscriptions.png',
                    text: 'subscription',
                },
                {
                    icon: 'src/assets/img/buy-comics-shop-locator.png',
                    text: 'comic shop locator',
                },
                {
                    icon: 'src/assets/img/buy-dc-power-visa.svg',
                    text: 'dc power visa',
                },
            ]
        }
    }

}
</script>

<template>
    <div class="wrapper">
        <div class="container">
            <ul>
                <li v-for="item in items">
                    <a href="#">
                        <BannerItems
                        class="item"
                        :icon="item.icon"
                        :text="item.text.toUpperCase()"
                        :alt="item.text"
                        />
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
@use '../assets/style/partials/mixins' as *;

.wrapper {
    background-color: $primary-color;
    .container {
        @include container($container-small);
        @include flex(row, center, center);
        ul {
            display: flex;
            .item {
                width: auto;
                padding: 20px 30px;
                :deep(img){
                    height: 50px;
                    width: 50px;
                    object-fit: contain;
                }
                :deep(h5){
                    color: #fff;
                    width: auto;
                    flex-shrink: 0;
                }
            }
        }
    }
}
</style>