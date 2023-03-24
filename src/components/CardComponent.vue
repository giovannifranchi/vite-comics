<script>
export default{
    name: 'CardComponent',
    props: {
        imgSrc: String,
        imgAlt: String,
        title: String,
    }
}
</script>

<template>
    <div>
        <img :src="imgSrc" :alt="imgAlt">
        <h3>{{ title }}</h3>
    </div>
</template>