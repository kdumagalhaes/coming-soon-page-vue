<template>
    <div class="content">
        <header class="content__logo">
            <Logo />
        </header>
        <div class="content__text">
            <HeroTitle text="We're" strong="coming soon" />
            <HeroParagraph
                text="Hello fellow shoppers! We're currently building our new fashion store. Add your email below to stay up-to-date with announcements and our launch deals."
            />
            <NewsForm />
        </div>
    </div>
</template>

<script>
//atoms
import { HeroTitle, HeroParagraph, NewsForm, Logo } from '@/components/atoms'

export default {
    components: {
        HeroTitle,
        HeroParagraph,
        NewsForm,
        Logo,
    },
}
</script>

<style lang="scss" scoped>
.content {
    width: 100%;
    max-width: 450px;
    margin: 40px;
    display: flex;
    flex-direction: column;
    justify-content: center;

    .content__logo {
        margin-bottom: 100px;
    }

    .content__text {
    }
}
</style>
