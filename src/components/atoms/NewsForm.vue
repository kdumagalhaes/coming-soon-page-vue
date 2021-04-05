<template>
    <form class="news-form" v-on:submit.prevent="checkEmail" novalidate>
        <label for="email">Email</label>
        <input
            v-model="email"
            type="email"
            name="email"
            placeholder="Email Address"
            autofocus
            v-bind:class="[errors.length ? 'alert' : '']"
        />
        <img
            class="error-icon"
            src="@/assets/img/icon-error.svg"
            alt="error icon"
            v-if="errors.length"
        />
        <button>
            <img src="@/assets/img/icon-arrow.svg" alt="send button" />
        </button>
        <p v-if="errors.length">{{ errors[0] }}</p>
    </form>
</template>

<script>
export default {
    data() {
        return {
            errors: [],
            email: null,
        }
    },

    methods: {
        checkEmail(email) {
            this.erros = []
            const re = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/

            if (!this.email) {
                this.errors.push('Email is empty')
            } else if (!re.test(email)) {
                this.errors.push('Please provide a valid email')
            }
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
        height: 60px;
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
        border: 1px solid red;
    }

    .error-icon {
        position: absolute;
        right: 100px;
        top: 35px;
    }
}
</style>
