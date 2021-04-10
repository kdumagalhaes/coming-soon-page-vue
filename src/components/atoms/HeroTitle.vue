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
    font-size: 3.6rem;
    letter-spacing: 1.5rem;
    line-height: 4.4rem;

    strong {
        color: $dark-grayish-red;
    }
}

@media only screen and (max-width: $mobile) {
    .hero-title {
        text-align: center;
        letter-spacing: 0;
        line-height: 3.3rem;
        font-size: 3rem;
    }
}
</style>
