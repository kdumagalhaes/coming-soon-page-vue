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
    font-size: 0.98rem;
    line-height: 32px;
    margin: 20px 0;
    font-weight: $semi-bold;
}
@media only screen and (max-width: $mobile) {
    .hero-paragraph {
        text-align: center;
        font-size: 0.88rem;
        line-height: 22px;
    }
}
</style>
