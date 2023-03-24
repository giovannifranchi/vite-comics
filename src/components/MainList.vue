<script>
import ButtonComponent from './ButtonComponent.vue';
import CardComponent from './CardComponent.vue';
export default {
    name: 'MainList',
    components: {
        CardComponent,
        ButtonComponent,
    },
    data(){
        return {
            cards: [
                        {
                          thumb: `https://picsum.photos/seed/picsum/200/300`,
                          price: "$19.99",
                          series: "Action Comics",
                          type: "comic book"
                        },
                        {
                          thumb: `https://picsum.photos/seed/picsum/200/300`,
                          price: "$3.99",
                          series: "American Vampire 1976",
                          type: "comic book"
                        },
                        {
                          thumb: `https://picsum.photos/seed/picsum/200/300`,
                          price: "$16.99",
                          series: "Aquaman",
                          type: "graphic novel"
                        },
                        {
                          thumb: `https://picsum.photos/seed/picsum/200/300`,
                          price: "$2.99",
                          series: "Batgirl",
                          type: "comic book"
                        },
                        {
                          thumb: `https://picsum.photos/seed/picsum/200/300`,
                          price: "$3.99",
                          series: "Batman",
                          type: "comic book"
                        },
                        {
                          thumb: `https://picsum.photos/seed/picsum/200/300`,
                          price: "$2.99",
                          series: "Batman Beyond",
                          type: "comic book"
                        },
                        {
                          thumb: `https://picsum.photos/seed/picsum/200/300`,
                          price: "$3.99",
                          series: "Batman/Superman",
                          type: "comic book"
                        },
                        {
                          thumb: `https://picsum.photos/seed/picsum/200/300`,
                          price: "$4.99",
                          series: "Batman/Superman Annual",
                          type: "comic book"
                        },
                        {
                          thumb: `https://picsum.photos/seed/picsum/200/300`,
                          price: "$5.99",
                          series: "Batman: The Joker War Zone",
                          type: "comic book"
                        },
                        {
                          thumb: `https://picsum.photos/seed/picsum/200/300`,
                          price: "$6.99",
                          series: "Batman: Three Jokers",
                          type: "comic book"
                        },
                        {
                          thumb: `https://picsum.photos/seed/picsum/200/300`,
                          price: "$4.99",
                          series: "Batman: White Knight Presents: Harley Quinn",
                          type: "comic book"
                        },
                        {
                          thumb: `https://picsum.photos/seed/picsum/200/300`,
                          price: "$16.99",
                          series: "Catwoman",
                          type: "graphic novel"
                        }
                    ], 
                    buttonText: 'LOAD MORE',                      
        }
    }
}
</script>

<template>
    <main>
        <div class="container">
            <CardComponent class="card" v-for="card in cards"
            :imgSrc="card.thumb"
            :imgAlt="card.series"
            :title="card.series"
            />
        </div>
        <div class="btn-container">
            <ButtonComponent class="btn" :text="buttonText"/>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;
@use '../assets/style/partials/mixins' as *;
main{
    background-color: $tertiary-color;
    .container {
        @include container($container-big);
        display: flex;
        flex-wrap: wrap;
        padding-top: 50px;
        .card{
            width: calc(100% / 6);
            padding: 20px;
            :deep(h3){
                padding-top: 20px;
                text-align: center;
                color:#fff;
            }
        }
        
    }
    .btn-container{
        display: flex;
        justify-content: center;
        .btn {
            width: 190px;
            background-color: $primary-color;
            padding: 10px 0;
            margin: 20px 0;
            color: #fff;
            font-weight: 600;
            border: 0;
            cursor: pointer;
            &:hover {
                background-color: darken($color: $primary-color, $amount: 15%);
            }
    }
    }
}
</style>