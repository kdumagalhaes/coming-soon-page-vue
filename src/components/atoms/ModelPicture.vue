<template>
    <img
        src="@/assets/img/hero-desktop.jpg"
        alt="Model picture"
        class="model-picture--desktop"
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
}
</style>
