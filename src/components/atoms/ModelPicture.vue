<template>
    <img
        src="@/assets/img/hero-desktop.jpg"
        alt="Model picture"
        class="model-picture--desktop"
    />
    <img
        src="@/assets/img/hero-mobile.jpg"
        alt="Model picture"
        class="model-picture--mobile"
    />
</template>

<style lang="scss" scoped>
.model-picture--desktop {
    max-height: 100vh;
    display: block;
}

.model-picture--mobile {
    display: none;
}

@media only screen and (max-width: $mobile) {
    .model-picture--desktop {
        max-height: 100vh;
        display: none;
    }
    .model-picture--mobile {
        display: block;
        width: 100%;
    }
}
</style>
