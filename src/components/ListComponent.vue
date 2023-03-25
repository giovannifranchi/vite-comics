<script>
export default {
    name: 'ListComponent',
    props: {
        title: String,
        options: Array,
    }
}
</script>

<template>
    <div>
        <h3>{{ title.toUpperCase() }}</h3>
        <ul>
            <li v-for="option in options">
                <a href="#">
                    {{ option}}
                </a>
            </li>
        </ul>
    </div>
</template>