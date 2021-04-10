<template>
    <div class="content">
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
import { HeroTitle, HeroParagraph, NewsForm } from '@/components/atoms'

export default {
    components: {
        HeroTitle,
        HeroParagraph,
        NewsForm,
    },
}
</script>

<style lang="scss" scoped>
.content {
    width: 100%;
    max-width: 470px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 0 20px;
}
</style>
