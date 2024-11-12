<template>
    <div>

        <Head title="Reset Password" />
        <div class="p-6 min-h-screen flex justify-center items-center bg-[#f5f5f5]">
            <flash-messages />
            <div class="w-full max-w-md">
                <form
                    class="mt-8 bg-white dark:bg-slate-900 border border-gray-100 rounded-lg shadow-xl overflow-hidden"
                    @submit.prevent="sendLink">
                    <div class="px-10 py-12">
                        <Link :href="route('home')">
                        <logo class="block mx-auto w-[195px] max-w-xs fill-white " />
                        </Link>
                        <h2 class="font-bold text-[20px] mt-10">{{ __('Reset Password') }}</h2>
                        <!-- <div class="mx-auto mt-3 w-24 border-b" /> -->
                        <text-input v-model="form.email" :error="form.errors.email" class="mt-5"
                            :label="__('Email Address')" type="email" autofocus autocapitalize="off" />
                        <loading-button :loading="form.processing"
                            class="ml-auto btn-indigo bg-custom-dark hover:bg-custom-dark w-full items-center justify-center mt-8"
                            type="submit">
                            {{ __('Send Password Reset Link') }}
                        </loading-button>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
import Logo from '@/Shared/Logo'
import TextInput from '@/Shared/TextInput'
import LoadingButton from '@/Shared/LoadingButton'
import { Head, Link } from '@inertiajs/vue3'
import FlashMessages from '@/Shared/FlashMessages'

export default {
    metaInfo: { title: 'Login' },
    components: {
        LoadingButton,
        Logo,
        TextInput,
        Head,
        Link,
        FlashMessages,
    },
    props: {
        is_demo: Number,
    },
    data() {
        return {
            form: this.$inertia.form({
                email: '',
            }),
        }
    },
    methods: {
        sendLink() {
            this.form.post(this.route('password.reset.email'))
        },
    },
}
</script>