<template>
    <div class="main-container">
        <div class="main-container__content">
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
import { ModelPicture } from '@/components/atoms'

export default {
    components: {
        Content,
        ModelPicture,
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
        align-items: center;
        margin: 0 auto;
    }
}
</style>
