<template>
    <div class="main-container">
        <div class="main-container__content">
            <Logo />
            <Content />
        </div>
        <div class="main-container__picture">
            <ModelPicture />
        </div>
    </div>
</template>

<script>
// molecules
import { Content } from '@/components/molecules'

// atoms
import { ModelPicture, Logo } from '@/components/atoms'

export default {
    components: {
        Content,
        ModelPicture,
        Logo,
    },
}
</script>

<style lang="scss" scoped>
.main-container {
    display: flex;
    justify-content: space-between;
    background-image: url('~@/assets/img/bg-pattern-desktop.svg');


    .main-container__content {
        display: flex;
        flex-direction: column;
        margin: 0 auto;
    }
}

@media only screen and (max-width: $mobile) {
    .main-container {
        flex-direction: column;
        background: green;
    }
}
</style>
