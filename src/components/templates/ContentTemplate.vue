<template>
    <main class="content-template">
        <div class="content-template__container">
            <Logo />
            <HeroTitle text="We're" strong="coming soon" />
            <HeroParagraph
                text="Hello fellow shoppers! We're currently building our new fashion store. 
            Add your email below to stay up-to-date with announcements and our launch deals."
            />
            <NewsForm />
        </div>
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
    padding: 40px 220px;
    width: 100%;
    background-image: url('~@/assets/img/bg-pattern-desktop.svg');

    .content_template__container {
        width: 700px;
        background-color: green;
    }
}
</style>
