<template>
    <div>

        <Head title="Contact" />
        <!-- Start Hero -->
        <section
            class="relative z-10 overflow-hidden bg-custom-dark pt-[120px] pb-[100px] md:pt-[130px] lg:pt-[160px] uppercase">
            <div class="container">
                <div class="-mx-4 flex flex-wrap items-center">
                    <div class="w-full px-4">
                        <div class="text-center">
                            <h1 class="lg:text-[32px] font-semibold text-white">{{ __(data.title) }}</h1>
                        </div>
                    </div>
                </div><!--end grid-->
            </div><!--end container-->
            <div>
                <span class="absolute top-0 left-0 z-[-1]">
                    <img src="/landing/images/header/shape-1.svg" alt="" />
                </span>
                <span class="absolute top-0 right-0 z-[-1]">
                    <img src="/landing/images/header/shape-2.svg" alt="" />
                </span>
            </div>
        </section><!--end section-->
        <!-- End Hero -->

        <!-- ====== Contact Section Start -->
        <section class="relative z-10 overflow-hidden bg-default-gray py-20 lg:py-[120px]">
            <div class="container mx-auto">
                <div class="-mx-4 flex flex-wrap lg:justify-between">
                    <div class="w-full px-4 lg:w-1/2 xl:w-6/12">
                        <div class="mb-12 max-w-[570px] lg:mb-0">
                            <h2 class="text-custom-dark mb-6 text-[32px] font-bold uppercase">
                                {{ page.content_text }}
                            </h2>
                            <p class="text-custom-dark mb-9 text-sm leading-relaxed">
                                {{ page.content_details }}
                            </p>
                            <div class="mb-8 flex w-full max-w-[370px]">
                                <div
                                    class="bg-primary text-custom-dark mr-6 flex h-[60px] w-full max-w-[60px] items-center justify-center overflow-hidden bg-opacity-5 sm:h-[70px] sm:max-w-[70px]">
                                    <icon name="home" class="w-8 h-8 fill-white" />
                                </div>
                                <div class="w-full">
                                    <h4 class="text-dark mb-1 text-xl font-bold">{{ 'Our Location' }}</h4>
                                    <p class="text-body-color text-base" v-html="sanitizeHtml(page.location)" />
                                </div>
                            </div>
                            <div class="mb-8 flex w-full max-w-[370px]">
                                <div
                                    class="bg-primary text-primary mr-6 flex h-[60px] w-full max-w-[60px] items-center justify-center overflow-hidden bg-opacity-5 sm:h-[70px] sm:max-w-[70px]">
                                    <icon name="phone" class="w-8 h-8 fill-white" />
                                </div>
                                <div class="w-full">
                                    <h4 class="text-custom-dark mb-1 text-[18px] font-bold">{{ 'Phone Number' }}</h4>
                                    <p class="text-body-color text-base">
                                        <a :href="'tel:' + page.phone">{{ page.phone
                                            }}</a>
                                    </p>
                                </div>
                            </div>
                            <div class="mb-8 flex w-full max-w-[370px]">
                                <div
                                    class="bg-primary text-primary mr-6 flex h-[60px] w-full max-w-[60px] items-center justify-center overflow-hidden bg-opacity-5 sm:h-[70px] sm:max-w-[70px]">
                                    <icon name="email" class="w-8 h-8 fill-white" />
                                </div>
                                <div class="w-full">
                                    <h4 class="text-dark mb-1 text-[18px] font-bold">{{ 'Email Address' }}</h4>
                                    <p class="text-body-color text-base">
                                        <a :href="'mailto:' + page.email">{{ page.email
                                            }}</a>
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="w-full px-4 lg:w-1/2 xl:w-5/12">
                        <div class="relative rounded-lg bg-white p-8 shadow-lg sm:p-12">
                            <form method="post" @submit.prevent="store">
                                <div class="mb-6">
                                    <input v-model="form.name" type="text" placeholder="Your Name"
                                        class="text-body-color border-[f0f0f0] focus:border-primary w-full rounded border py-3 px-[14px] text-base outline-none focus-visible:shadow-none"
                                        required />
                                </div>
                                <div class="mb-6">
                                    <input v-model="form.email" type="email" placeholder="Your Email"
                                        class="text-body-color border-[f0f0f0] focus:border-primary w-full rounded border py-3 px-[14px] text-base outline-none focus-visible:shadow-none"
                                        required />
                                </div>
                                <div class="mb-6">
                                    <input v-model="form.phone" type="text" placeholder="Your Phone"
                                        class="text-body-color border-[f0f0f0] focus:border-primary w-full rounded border py-3 px-[14px] text-base outline-none focus-visible:shadow-none" />
                                </div>
                                <div class="mb-4">
                                    <textarea v-model="form.message" rows="6" placeholder="Your Message"
                                        class="text-body-color border-[f0f0f0] focus:border-primary w-full resize-none rounded border py-3 px-[14px] text-base outline-none focus-visible:shadow-none"
                                        required />
                                </div>
                                <div class="flex justify-center items-center pb-3">
                                    <vue-recaptcha v-if="site_key" ref="vueRecaptcha" :sitekey="site_key" size="normal"
                                        theme="light" @verify="recaptchaVerified" @expire="recaptchaExpired"
                                        @fail="recaptchaFailed" @error="recaptchaError" />
                                </div>
                                <div>
                                    <button :disabled="disabled && site_key" type="submit"
                                        class="bg-custom-dark border-primary w-full border py-2 text-white transition hover:bg-opacity-90 cursor-pointer"
                                        :class="{ 'disabled': disabled && site_key }">
                                        Send Message
                                    </button>
                                </div>
                            </form>
                            <div>
                                <span class="absolute -top-10 -right-9 z-[-1]">
                                    <img src="/landing/images/contact/shape-1.svg" alt="" />
                                </span>
                                <span class="absolute -right-10 top-[90px] z-[-1]">
                                    <img src="/landing/images/contact/shape-2.svg" alt="" />

                                </span>
                                <span class="absolute -left-7 -bottom-7 z-[-1]">
                                    <img src="/landing/images/contact/shape-3.svg" alt="" />

                                </span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <!-- ====== Contact Section End -->
    </div>
</template>
<script>
import Layout from '@/Shared/Landing/Layout'
import Icon from '@/Shared/Icon'
import { Head } from '@inertiajs/vue3'
import sanitizeHtml from 'sanitize-html'
import vueRecaptcha from 'vue3-recaptcha2'
export default {
    components: {
        vueRecaptcha,
        Icon,
        Head,
    },
    layout: Layout,
    props: {
        data: Object,
        site_key: String,
    },
    data() {
        return {
            disabled: true,
            page: JSON.parse(this.data.html),
            form: this.$inertia.form({
                name: '',
                email: '',
                phone: '',
                message: '',
            }),
        }
    },
    methods: {
        recaptchaVerified(response) {
            this.disabled = false
        },
        recaptchaExpired() {
            this.$refs.vueRecaptcha.reset()
        },
        recaptchaFailed() {
        },
        recaptchaError(reason) {
            console.log(reason)
        },
        sanitizeHtml: sanitizeHtml,
        store() {
            this.form.post(this.route('contact.send'), {
                onSuccess: () => {
                    this.form.reset()
                },
            })
        },
    },
}
</script>
