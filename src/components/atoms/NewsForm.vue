<template>
    <form class="news-form" v-on:submit.prevent="submitForm" novalidate>
        <label for="email">Email</label>
        <input
            v-model="email"
            type="email"
            name="email"
            placeholder="Email Address"
            v-bind:class="[errors.length ? 'alert' : '']"
            @blur="errors = []"
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
        <p v-if="errors.length">
            {{ errors[0] }}
        </p>
    </form>
</template>

<script>
export default {
    data() {
        return {
            regex: /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/,
            errors: [],
            email: null,
        }
    },

    methods: {
        submitForm() {
            this.errors = []
            if (!this.validEmail(this.email)) {
                this.errors.push('Please provide a valid email')
            } else {
                this.errors = []
            }
        },
        validEmail(email) {
            return this.regex.test(email)
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
        color: $alert-red;
        padding: 10px 30px;
        font-size: 0.9rem;
    }

    .alert {
        border: 2px solid $alert-red;
    }

    .error-icon {
        position: absolute;
        right: 100px;
        top: 29px;
    }
}
</style>
