<template>
    <main class="content-template">
        <Logo />
        <HeroTitle text="We're" strong="coming soon" />
        <HeroParagraph
            text="We're currently building our new fashion store. 
            Add your email below to stay up-to-date with announcements and our launch deals."
        />
        <NewsForm />
    </main>
</template>

<script>
// components
import { Logo, HeroParagraph, HeroTitle, NewsForm } from '@/components/atoms'
export default {
    components: {
        Logo,
        NewsForm,
        HeroTitle,
        HeroParagraph,
    },
}
</script>

<style lang="scss" scoped>
.content-template {
    padding: 40px;
    width: 100%;
    max-width: 600px;
}
</style>
