<template>
    <h1 class="hero-title">
        {{ text }} <strong>{{ strong }}</strong>
    </h1>
</template>

<script>
export default {
    props: {
        text: String,
        strong: String,
    },
}
</script>

<style lang="scss" scoped>
.hero-title {
    text-transform: uppercase;
    font-weight: $light;
    color: $desaturated-red;
    font-size: 4rem;

    strong {
        color: $dark-grayish-red;
    }
}
</style>
