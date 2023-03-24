<script>
export default {
    name: 'Header-list',
    data(){
        return {
            menuList: [
                {
                    option: 'characters',
                    link: '#',
                    isActive: false,
                },
                {
                    option: 'comics',
                    link: '#',
                    isActive: false,
                },
                {
                    option: 'movies',
                    link: '#',
                    isActive: false,
                },
                {
                    option: 'tv',
                    link: '#',
                    isActive: false,
                },
                {
                    option: 'games',
                    link: '#',
                    isActive: false,
                },
                {
                    option: 'collectibles',
                    link: '#',
                    isActive: false,
                },
                {
                    option: 'videos',
                    link: '#',
                    isActive: false,
                },
                {
                    option: 'fans',
                    link: '#',
                    isActive: false,
                },
                {
                    option: 'news',
                    link: '#',
                    isActive: false,
                },
                {
                    option: 'shop',
                    link: '#',
                    isActive: false,
                },
            ]
        }
    }, 
    methods: {
        changeActive(index){
            this.menuList.forEach((item, i)=> {
                if(i === index){
                    item.isActive = true;
                }else{
                    item.isActive = false;
                }
            });
        }
    }
}
</script>

<template>
    <ul>
        <li v-for="(item, index) in menuList" @click="changeActive(index)" :class="item.isActive ? 'active' : '' ">
            <a :href="item.link">{{ item.option.toUpperCase() }}</a>
        </li>
    </ul>
</template>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
@use '../assets/style/partials/mixins' as *;

ul {
    display: flex;
    gap: 40px;
    li{
        @include flex(row, center, center);
        padding: 20px 0;
        color: $text-color;
        &:not(.active):hover {
            color: lighten($color: $text-color, $amount: 15%);
        }
    }
    .active {
        color: $primary-color;
        border-bottom: 3px solid $primary-color;

    }
}
</style>