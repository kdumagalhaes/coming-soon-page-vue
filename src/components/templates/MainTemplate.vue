<template>
    <div class="main-template">
        <ContentTemplate />
        <ModelPicture />
    </div>
</template>

<script>
// components
import { ModelPicture } from '@/components/atoms'
import ContentTemplate from './ContentTemplate'

export default {
    components: {
        ModelPicture,
        ContentTemplate,
    },
}
</script>

<style lang="scss" scoped>
.main-template {
    display: flex;
    height: 100vh;
}
</style>
