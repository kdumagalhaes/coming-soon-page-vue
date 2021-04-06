<template>
    <form class="news-form" v-on:submit.prevent novalidate>
        <label for="email">Email</label>
        <input
            v-model="email"
            type="email"
            name="email"
            placeholder="Email Address"
            v-bind:class="[!validEmail ? 'alert' : '']"
        />
        <img
            class="error-icon"
            src="@/assets/img/icon-error.svg"
            alt="error icon"
            v-if="!validEmail"
        />
        <button>
            <img src="@/assets/img/icon-arrow.svg" alt="send button" />
        </button>
        <p v-if="!validEmail">Please provide a valid email</p>
    </form>
</template>

<script>
export default {
    data() {
        return {
            email: '',
            regex: /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/,
        }
    },

    computed: {
        validEmail() {
            return this.regex.test(this.email)
        },
    },
}
</script>

<style lang="scss" scoped>
.news-form {
    position: relative;

    input,
    button {
        border-radius: 50px;
        height: 50px;
    }

    input {
        border: 1px solid $desaturated-red;
        padding-left: 30px;
        width: 100%;

        &::placeholder {
            color: $desaturated-red;
            font-family: 'Poppins', sans-serif;
        }
    }

    button {
        width: 90px;
        background: $gradient2;
        border: none;
        position: absolute;
        right: 0;
        -webkit-box-shadow: -9px 6px 15px 3px rgba(99, 52, 52, 0.24);
        box-shadow: -9px 6px 15px 3px rgba(99, 52, 52, 0.24);
        transition: 0.4s all;

        &:hover {
            -webkit-box-shadow: -9px 6px 15px -2px rgba(99, 52, 52, 0.24);
            box-shadow: -9px 6px 15px -2px rgba(99, 52, 52, 0.24);
        }
    }

    label {
        font-size: 1px;
    }

    p {
        color: red;
        padding: 10px 30px;
        font-size: 0.9rem;
    }

    .alert {
        border: 2px solid red;
    }

    .error-icon {
        position: absolute;
        right: 100px;
        top: 30px;
    }
}
</style>
