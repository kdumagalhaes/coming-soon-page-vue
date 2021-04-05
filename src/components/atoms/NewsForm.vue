<template>
    <form class="news-form" v-on:submit.prevent>
        <input type="email" name="" id="" placeholder="Email Address" />
        <button>
            <img src="@/assets/img/icon-arrow.svg" alt="send button" />
        </button>
    </form>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.news-form {
    width: 400px;
    position: absolute;

    input,
    button {
        border-radius: 50px;
        height: 60px;
    }

    input {
        border: 1px solid $desaturated-red;
        padding: 0 95px 0 20px;
        width: 100%;
        position: absolute;

        &::placeholder {
            color: $desaturated-red;
            font-family: 'Poppins', sans-serif;
        }
    }

    button {
        width: 90px;
        background: $gradient2;
        border: none;
        float: right;
        position: relative;
    }
}
</style>
