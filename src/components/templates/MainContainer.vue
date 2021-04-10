<template>
    <div class="main-container">
        <div class="main-container__content">
            <Logo />
            <div class="main-container__content--picture-mobile">
                <ModelPictureMobile />
            </div>
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
import { ModelPicture, Logo, ModelPictureMobile } from '@/components/atoms'

export default {
    components: {
        Content,
        ModelPicture,
        ModelPictureMobile,
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

        .main-container__content--picture-mobile {
            display: none;
            margin-bottom: 60px;
        }
    }
}

@media only screen and (max-width: $mobile) {
    .main-container {
        flex-direction: column;
        height: 100vh;

        .main-container__content {
            .main-container__content--picture-mobile {
                display: block;
            }
        }
    }
}
</style>
