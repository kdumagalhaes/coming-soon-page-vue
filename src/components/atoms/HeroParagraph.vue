<template>
    <p class="hero-paragraph">{{ text }}</p>
</template>

<script>
export default {
    props: {
        text: String,
    },
}
</script>

<style lang="scss" scoped>
.hero-paragraph {
    color: $desaturated-red;
    width: 100%;
}
</style>
