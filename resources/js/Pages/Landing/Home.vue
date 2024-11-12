<template>
    <div>
        <!-- Start Hero -->

        <Head :title="__('Home')" />
        <!-- ====== Hero Section Start -->
        <div id="home" class="relative overflow-hidden pt-[120px] md:pt-[130px] lg:pt-[160px] uppercase">
            <div class="container">
                <div class="-mx-4 flex flex-wrap items-center">
                    <div class="w-full px-4">
                        <div class="hero-content wow fadeInUp ml-auto max-w-[780px] text-right" data-wow-delay=".2s">
                            <h1 class="lg:mt-10 mb-8 text-3xl font-bold leading-snug text-white sm:text-4xl sm:leading-snug md:text-[45px] md:leading-snug"
                                v-html="sanitizeHtml(html.sections[0].title)" />
                            <p class="ml-auto mb-10 max-w-[600px] text-base text-[#e4e4e4] sm:text-lg sm:leading-relaxed md:text-xl md:leading-relaxed"
                                v-html="sanitizeHtml(html.sections[0].details)" />
                            <ul class="mb-10 flex flex-wrap items-right justify-end gap-6">
                                <li v-for="(button, bi) in html.sections[0].buttons" :key="bi">
                                    <!-- <Link :href="button.link"
                                        class="inline-flex items-center justify-center bg-white py-4 px-6 text-center text-base font-medium text-dark transition duration-300 ease-in-out hover:text-primary hover:shadow-lg sm:px-10">
                                    {{ button.text }}
                                    </Link> -->
                                    <Link :href="button.link"
                                        class="inline-flex items-center justify-center bg-transparent border border-white py-2 px-6 text-center text-base font-medium text-white transition duration-300 ease-in-out hover:bg-white hover:text-black hover:shadow-lg sm:px-10">
                                    {{ button.text }}
                                    </Link>
                                </li>
                            </ul>
                        </div>
                    </div>

                    <!-- <div class="w-full px-4">
                        <div class="wow fadeInUp relative z-10 mx-auto max-w-[845px]" data-wow-delay=".25s">
                            <div class="mt-16">
                                <img v-if="html.sections[0].image" :src="html.sections[0].image" alt=""
                                    class="mx-auto max-w-full rounded-t-xl rounded-tr-xl" />
                                <img v-else src="/landing/images/dashboard-helpdesk.png" alt=""
                                    class="mx-auto max-w-full rounded-t-xl rounded-tr-xl" />
                            </div>
                            <div class="absolute bottom-0 -left-9 z-[-1]">
                                <img src="/images/svg/dot-1.svg" alt="dot" />
                            </div>
                            <div class="absolute -top-6 -right-6 z-[-1]">
                                <img src="/images/svg/dot-2.svg" alt="dot" />
                            </div>
                        </div>
                    </div> -->
                </div>
            </div>
        </div>
        <section class="pt-20 pb-8 lg:pt-[120px] lg:pb-[70px] uppercase">
            <div class="container">
                <div class="-mx-4 flex flex-wrap">
                    <div class="w-full px-4">
                        <div class="mb-12 max-w-[650px] lg:mb-20">
                            <span class="mb-2 block text-lg font-semibold text-primary">
                                {{ html.sections[1].tagline }}
                            </span>
                            <h2 class="mb-4 text-3xl font-bold text-dark sm:text-4xl md:text-[42px]">
                                {{ html.sections[1].title }}
                            </h2>
                            <p class="text-lg leading-relaxed text-body-color sm:text-xl sm:leading-relaxed"
                                v-html="html.sections[1].details" />
                        </div>
                    </div>
                </div>
                <div v-if="html.sections[1]" class="-mx-4 flex flex-wrap">
                    <div v-for="(feature, fi) in html.sections[1].features" :key="fi"
                        class="w-full px-4 md:w-1/2 lg:w-1/4">
                        <div class="wow fadeInUp group mb-12 bg-white" data-wow-delay=".1s">
                            <div
                                class="relative z-10 mb-8 flex h-[70px] w-[70px] items-center justify-center bg-primary">
                                <span
                                    class="absolute top-0 left-0 z-[-1] mb-8 flex h-[70px] w-[70px] rotate-[25deg] items-center justify-center bg-custom-dark bg-opacity-20 duration-300 group-hover:rotate-45" />
                                <icon :name="feature.icon" class="w-8 h-8 fill-white" />
                            </div>
                            <h4 class="mb-3 text-xl font-bold text-dark">
                                {{ feature.title }}
                            </h4>
                            <p class="mb-8 text-body-color lg:mb-11" v-html="feature.details" />
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <!-- Start -->
        <section v-if="html.sections[2].enable_ticket_section" id="ticketSubmit"
            class="relative md:py-24 py-16 bg-default-gray dark:bg-slate-800 uppercase">
            <div class="container">
                <form class="card mt-2 p-4 rounded shadow-xl overflow-hidden" enctype="multipart/form-data"
                    @submit.prevent="store">
                    <div class="px-5 ">
                        <h1
                            class="py-5 text-center md:text-3xl text-2xl md:leading-normal leading-normal font-semibold">
                            {{ __('Create a ticket') }}
                        </h1>
                        <div class="mx-auto mb-6 mt-1 w-24 border-b" />
                        <div class="flex flex-wrap">
                            <text-input v-model="form.first_name" :error="form.errors.last_name"
                                class="lg:pr-6 rtl:pr-0 rtl:pl-6 pb-5 md:col-span-6 w-full lg:w-1/2"
                                :label="__('First name')" />
                            <text-input v-model="form.last_name" :error="form.errors.last_name"
                                class="lg:pr-6 rtl:pr-0 rtl:pl-6 pb-5 md:col-span-6 w-full lg:w-1/2"
                                :label="__('Last name')" />
                            <text-input v-model="form.email" :error="form.errors.email"
                                class="lg:pr-6 rtl:pr-0 rtl:pl-6 pb-5 md:col-span-6 w-full lg:w-1/2"
                                :label="__('Email Address')" />


                            <!-- <select-input v-model="form.department_id" :error="form.errors.department_id"
                                class="pr-6 rtl:pr-0 rtl:pl-6 pb-5 md:col-span-6 lg:w-1/3" :label="__('Department')">
                                <option :value="null">{{ __('Select a department') }}</option>
                                <option v-for="department in departments" :key="department.id" :value="department.id">{{
                                    department.name }}</option>
                            </select-input> -->

                            <select-input v-model="form.type_id" :error="form.errors.type_id"
                                class="lg:pr-6 rtl:pr-0 rtl:pl-6 pb-5 md:col-span-6 w-full lg:w-1/2"
                                :label="__('Ticket type')">
                                <option :value="null">{{ __('Select a type') }}</option>
                                <option v-for="type in types" :key="type.id" :value="type.id">{{ type.name }}</option>
                            </select-input>

                            <text-input v-model="form.subject" :error="form.errors.subject" class=" pb-5 w-full"
                                :label="__('Subject')" />

                            <!-- <select-input v-model="form.category_id" :error="form.errors.category_id"
                                class=" pb-5 md:col-span-6 lg:w-1/3" :label="__('Category')">
                                <option :value="null">{{ __('Select a category') }}</option>
                                <option v-for="category in categories" :key="category.id" :value="category.id">
                                    {{
                                    category.name }}
                                </option>
                            </select-input> -->

                            <div class=" pt-2 pb-8 w-full">
                                <label class="form-label">{{ __('Request Details') }}</label>
                                <ckeditor id="ticketDetails" v-model="form.details" :editor="editor"
                                    :error="form.errors.details" :config="editorConfig" />
                            </div>
                        </div>

                        <!-- Attachments -->
                        <input ref="file" type="file"
                            accept=".xlsx,.xls,image/*,.doc, .docx,.ppt, .pptx,.txt,.pdf, .zip" class="hidden"
                            multiple="multiple" @change="fileInputChange" />
                        <div class="pr-6 rtl:pl-6 pb-8 w-full lg:w-full flex-col">
                            <button type="button" class="btn flex justify-center items-center border-0"
                                @click="fileBrowse">
                                <icon name="file" class="flex-shrink-0 h-8 fill-gray-400 pr-2 rtl:pl-2" />
                                <h4>{{ __('Attach files') }}</h4>
                            </button>
                            <div v-for="(file, fi) in form.files" v-if="form.files.length" :key="fi"
                                class="flex items-center justify-between pr-6 pt-8 w-full lg:w-1/2">
                                <div class="flex-1 pr-1">
                                    {{ file.name }} <span class="text-gray-500 text-xs">({{ getFileSize(file.size)
                                        }})</span>
                                </div>
                                <button type="button" class="btn flex justify-center items-center"
                                    @click="fileRemove(file, fi)">
                                    {{ __('Remove') }}
                                </button>
                            </div>
                        </div>
                        <!-- Attachments -->
                        <div class="flex items-start mb-5">
                            <div class="flex items-center h-5">
                                <input id="terms" v-model="accept_terms" type="checkbox"
                                    class="w-4 h-4 border border-gray-300 rounded bg-gray-50 focus:ring-3 focus:ring-blue-300 dark:bg-gray-700 dark:border-gray-600 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800"
                                    required />
                            </div>
                            <label for="terms" class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300">I agree
                                with the <a :href="route('terms_service')" target="_blank"
                                    class="text-blue-600 hover:underline dark:text-blue-500">terms and
                                    conditions</a></label>
                        </div>
                    </div>
                    <div class="px-4 py-4 border-t border-gray-100 flex justify-end">
                        <loading-button :loading="form.processing"
                            class="bg-custom-dark py-2 px-6 text-base font-medium text-white duration-300 ease-in-out hover:bg-opacity-80"
                            type="submit">
                            Submit
                        </loading-button>
                    </div>
                </form>
            </div><!--end container-->
        </section><!--end section-->
        <!-- End -->
    </div>
</template>

<script>
import { Head, Link } from '@inertiajs/vue3'
import Logo from '@/Shared/Logo'
import Layout from '@/Shared/Landing/Layout'
import Icon from '@/Shared/Icon'
import TextInput from '@/Shared/TextInput'
import SelectInput from '@/Shared/SelectInput'
import LoadingButton from '@/Shared/LoadingButton'
import ClassicEditor from '@ckeditor/ckeditor5-build-classic'
import sanitizeHtml from 'sanitize-html'
import UploadAdapter from '@/Shared/UploadAdapter'
import CKEditor from '@ckeditor/ckeditor5-vue'

export default {
    metaInfo: { title: 'Home' },
    components: {
        Logo,
        Icon,
        LoadingButton,
        SelectInput,
        TextInput,
        Head,
        Link,
        ckeditor: CKEditor.component,
    },
    layout: Layout,
    props: {
        categories: Array,
        departments: Array,
        types: Array,
        title: String,
        page: Object,
        auth: Object,
    },
    remember: 'form',
    data() {
        return {
            editor: ClassicEditor,
            accept_terms: false,
            html: JSON.parse(this.page.html),
            editorConfig: {
                toolbar: ['heading', '|', 'bold', 'italic', 'link', 'bulletedList', 'numberedList', '|', 'outdent', 'indent', '|', 'insertTable', 'blockQuote', '|', 'imageUpload', 'mediaEmbed', '|', 'undo', 'redo'],
                table: {
                    toolbar: ['tableColumn', 'tableRow', 'mergeTableCells'],
                },
                extraPlugins: [this.uploader],
            },
            form: this.$inertia.form({
                first_name: '',
                last_name: '',
                email: '',
                department_id: 1,
                category_id: 1,
                type_id: null,
                subject: null,
                details: '',
                files: [],
            }),
            sanitizeHtml: sanitizeHtml,
        }
    },
    created() {
        if (this.auth.user) {
            this.form.first_name = this.auth.user.first_name
            this.form.last_name = this.auth.user.last_name
            this.form.email = this.auth.user.email
        }
    },

    methods: {
        uploader(editor) {
            editor.plugins.get('FileRepository').createUploadAdapter = (loader) => {
                return new UploadAdapter(loader)
            }
        },
        uploadFiles() {
            this.form.files = this.$refs.files.files
        },
        store() {
            if (!this.accept_terms) {
                alert('You must need to accept the terms and condition.')
            }
            this.form.post(this.route('ticket_store'), {
                onSuccess: () => {
                    this.form.reset()
                },
                // form.reset()
            })
        },
        fileInputChange(e) {
            let selectedFiles = e.target.files
            for (let i = 0; i < selectedFiles.length; i++) {
                this.form.files.push(selectedFiles[i])
            }
        },
        fileRemove(image, index) {
            this.form.files.splice(index, 1)
        },
        getFileSize(size) {
            const i = Math.floor(Math.log(size) / Math.log(1024))
            return (size / Math.pow(1024, i)).toFixed(2) * 1 + ' ' + ['B', 'kB', 'MB', 'GB', 'TB'][i]
        },
        fileBrowse() {
            this.$refs.file.click()
        },
    },
}
</script>

<style scoped>
#home {
    background-image: url('/landing/images/hero_img.jpg');
    background-size: cover;
    background-position: center;
    height: 55vh;
    /* Default height for small screens */
}

#home::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    /* Overlay color */
    z-index: 1;
}

#home>* {
    position: relative;
    z-index: 2;
}

@media (min-width: 768px) {
    #home {
        height: 70vh;
        /* Height for medium screens */
    }
}

@media (min-width: 1024px) {
    #home {
        height: 90vh;
        /* Height for large screens */
    }
}

@media (min-width: 1280px) {
    #home {
        height: 100vh;
        /* Height for extra large screens */
    }
}
</style>