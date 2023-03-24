<script>
export default {
    name: 'ButtonComponent',
    props: {
        text: String,
        color: String,
    }
}
</script>

<template>
    <button type="button">
        {{ text }}
    </button>
</template>

