<!--
<template>
    <footer class="wow fadeInUp relative z-10 bg-footer-black pt-20 lg:pt-[80px]" data-wow-delay=".15s">
        <div class="container">
            <div class="-mx-4 flex flex-wrap">
                <div class="w-full px-4 sm:w-1/2 md:w-1/2 lg:w-3/12 xl:w-3/12">
                    <div class="mb-10 w-full">
                        <Link :href="route('home')" class="mb-6 inline-block max-w-[160px]">
                        <logo class="help-desk-logo" />
                        </Link>
                        <p class="mb-7 text-base text-[#f3f4fe]" v-html="footer_text" />
                    </div>
                </div>
                <div class="w-full px-4 sm:w-1/2 md:w-1/2 lg:w-3/12 xl:w-3/12">
                    <div class="mb-10 w-full">
                        <h4 class="mb-9 text-lg font-semibold text-white">Company</h4>
                        <ul>
                            <li v-if="!!enable_option && enable_option.show_login">
                                <a :href="route('login')"
                                    class="mb-2 inline-block text-base leading-loose text-[#f3f4fe] hover:text-primary">
                                    Login</a>
                            </li>
                            <li v-if="!!enable_option && enable_option.show_login">
                                <a :href="route('register')"
                                    class="mb-2 inline-block text-base leading-loose text-[#f3f4fe] hover:text-primary">
                                    Register</a>
                            </li>
                            <li v-if="!!enable_option && enable_option.blog">
                                <a :href="route('blog')"
                                    class="mb-2 inline-block text-base leading-loose text-[#f3f4fe] hover:text-primary">
                                    Blog
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="w-full px-4 sm:w-1/2 md:w-1/2 lg:w-3/12 xl:w-3/12">
                    <div class="mb-10 w-full">
                        <h4 class="mb-9 text-lg font-semibold text-white">Usefull Links</h4>
                        <ul>
                            <li>
                                <a :href="route('terms_service')"
                                    class="mb-2 inline-block text-base leading-loose text-[#f3f4fe] hover:text-primary">
                                    Terms of Services</a>
                            </li>
                            <li>
                                <a :href="route('privacy')"
                                    class="mb-2 inline-block text-base leading-loose text-[#f3f4fe] hover:text-primary">
                                    Privacy Policy</a>
                            </li>
                            <li v-if="!!enable_option && enable_option.kb">
                                <a :href="route('kb')"
                                    class="mb-2 inline-block text-base leading-loose text-[#f3f4fe] hover:text-primary">
                                    Knowledge Base
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="w-full px-4 sm:w-1/2 md:w-1/2 lg:w-3/12 xl:w-3/12">
                    <div class="mb-10 w-full">
                        <h4 class="mb-9 text-lg font-semibold text-white">Newsletter</h4>
                        <p class="mt-5 text-white">Join our newsletter service.</p>
                        <form @submit.prevent="subscribe">
                            <div class="grid grid-cols-1">
                                <div class="foot-subscribe my-3">
                                    <label class="form-label text-white">Your email address <span
                                            class="text-red-600">*</span></label>
                                    <div class="form-icon relative mt-2 text-white">
                                        <icon class="w-4 w-4 absolute top-3 left-4 z-1 fill-gray-800"
                                            name="send_plan" />
                                        <input v-model="form.email" type="email"
                                            class="form-input bg-gray-800 border border-white pl-12 focus:shadow-none"
                                            placeholder="Email" name="email" required="" />
                                    </div>
                                </div>

                                <loading-button :loading="form.processing"
                                    class="rounded-lg bg-primary py-3 px-6 text-base font-medium justify-center text-white duration-300 ease-in-out hover:bg-opacity-80"
                                    type="submit">{{ __('Submit') }}</loading-button>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>

        <div class="mt-12 border-t border-opacity-40 py-8 lg:mt-[60px]">
            <div class="container">
                <div class="-mx-4 flex flex-wrap justify-center">
                    <div class="my-1 flex justify-center ">
                        <p class="text-base text-center text-[#f3f4fe]" v-html="footer_content.copyright" />
                    </div>
                </div>
            </div>
        </div>

        <div>
            <span class="absolute left-0 top-0 z-[-1]">
                <img src="/landing/images/footer/shape-1.svg" alt="" />
            </span>

            <span class="absolute bottom-0 right-0 z-[-1]">
                <img src="/landing/images/footer/shape-3.svg" alt="" />
            </span>

            <span class="absolute top-0 right-0 z-[-1]">
                <img src="/landing/images/footer/shape-2.svg" alt="" />
            </span>
        </div>
    </footer>
</template> -->

<script>
// import Logo from '@/Shared/Logo'
// import Icon from '@/Shared/Icon'
// import LoadingButton from '@/Shared/LoadingButton'
// import { Link } from '@inertiajs/vue3'
// export default {
//     components: {
//         Logo, LoadingButton, Link, Icon
//     },
//     props: {
//         footer: Object,
//     },
//     data() {
//         return {
//             footer_content: this.footer ? JSON.parse(this.footer.html) : [],
//             footer_text: this.footer ? JSON.parse(this.footer.html).text: 'Start working with HelpDesk that can provide everything you need to generate awareness, drive traffic, connect.',
//             form: this.$inertia.form({
//                 email: '',
//             }),
//             enable_option: {},
//         }
//     },
//     methods: {
//         subscribe() {
//             this.form.post(this.route('subscribe.news'))
//             this.form.email = ''
//         },
//     },
//     created() {
//         if(this.$page.props.enable_options){
//             let options = JSON.parse(this.$page.props.enable_options.value)
//             options.forEach(option=>{
//                 this.enable_option[option.slug] = !!option.value
//             })
//         }
//     }

// }
import Icon from '@/Shared/Icon'

export default {
    components: {
        Icon,
    },
}
</script>

<template>
    <footer class="footer">
        <div class="footer-container">
            <div class="footer-column">
                <h4><strong>COMPANY</strong></h4>
                <ul>
                    <li><a href="https://droppiez.com/pages/about-droppiez">About Droppiez</a></li>
                    <li>
                        <a href="https://hello.droppiez.com/terms-of-services">Terms
                            of Services</a>
                    </li>
                    <li>
                        <a href="https://hello.droppiez.com/privacy">Privacy
                            Policy</a>
                    </li>
                    <li><a href="#">Sustainability</a></li>
                </ul>
                <address>
                    <strong>Droppiez Head Office</strong><br />
                    12700 Nicollet Ave, Burnsville,<br />
                    MINNESOTA 55337, United States
                </address>
            </div>
            <div class="footer-column">
                <h4><strong>SUPPORT</strong></h4>
                <ul>
                    <li>
                        <a href="https://hello.droppiez.com/faq">FAQs</a>
                    </li>
                    <li>
                        <a href="https://hello.droppiez.com/contact">Return
                            & Exchange</a>
                    </li>
                    <li><a href="#">Contact</a></li>
                    <li>
                        <a href="https://hello.droppiez.com/">Support
                            Login</a>
                    </li>
                </ul>
            </div>
            <div class="footer-column">
                <h4><strong>PLUG INTO THE DROP!</strong></h4>
                <p>
                    Get the latest drops, exclusive deals, and all things straight to your inbox.
                </p>
                <p class="mt-3 mb-4">
                    <strong>No noise, just the essentials.</strong> Tap in and keep it lowkey legendary.
                </p>
                <form>
                    <input type="email" placeholder="E-mail" />
                    <button class="mt-4" type="submit">SUBSCRIBE</button>
                </form>
            </div>
            <div class="footer-column">
                <h4><strong>EXPLORE</strong></h4>
                <ul>
                    <li><a href="https://droppiez.com/collections/mens-hoodies">Men's Hoodies</a></li>
                    <li><a href="https://droppiez.com/collections/womens-hoodies">Women's Hoodies</a></li>
                    <li><a href="https://droppiez.com/collections/mena-sweatshirts">Men's Sweatshirts</a></li>
                    <li><a href="https://droppiez.com/collections/mens-long-sleeved">Men's Long Sleeves</a></li>
                    <li><a href="https://droppiez.com/collections/womens-sweatshirts">Women's Sweatshirts</a></li>
                    <li><a href="https://droppiez.com/collections/womens-long-sleeved">Women's Long Sleeves</a></li>
                    <li><a href="https://droppiez.com/collections/unisex-hoodie">Unisex Hoodies</a></li>
                    <li><a href="https://droppiez.com/collections/unisex-sweatshirts">Unisex Sweatshirts</a></li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="social-icons inline-grid grid-cols-12 gap-8 mt-10 mb-10">
                <a href="https://www.facebook.com/droppiez">
                    <svg aria-hidden="true" focusable="false" width="24" class="icon icon-facebook" viewBox="0 0 24 24">
                        <path fill-rule="evenodd" clip-rule="evenodd"
                            d="M10.183 21.85v-8.868H7.2V9.526h2.983V6.982a4.17 4.17 0 0 1 4.44-4.572 22.33 22.33 0 0 1 2.667.144v3.084h-1.83a1.44 1.44 0 0 0-1.713 1.68v2.208h3.423l-.447 3.456h-2.97v8.868h-3.57Z"
                            fill="currentColor" />
                    </svg>
                </a>
                <a href="https://x.com/droppiez_store">
                    <svg aria-hidden="true" focusable="false" width="24" class="icon icon-twitter" viewBox="0 0 24 24">
                        <path
                            d="M16.94 4h2.715l-5.93 6.777L20.7 20h-5.462l-4.278-5.593L6.065 20H3.35l6.342-7.25L3 4h5.6l3.868 5.113L16.94 4Zm-.952 14.375h1.504L7.784 5.54H6.17l9.818 12.836Z"
                            fill="currentColor" />
                    </svg>
                </a>
                <a href="https://www.instagram.com/droppiez.store">
                    <svg aria-hidden="true" focusable="false" width="24" class="icon icon-instagram"
                        viewBox="0 0 24 24">
                        <path fill-rule="evenodd" clip-rule="evenodd"
                            d="M12 2.4c-2.607 0-2.934.011-3.958.058-1.022.046-1.72.209-2.33.446a4.705 4.705 0 0 0-1.7 1.107 4.706 4.706 0 0 0-1.108 1.7c-.237.611-.4 1.31-.446 2.331C2.41 9.066 2.4 9.392 2.4 12c0 2.607.011 2.934.058 3.958.046 1.022.209 1.72.446 2.33a4.706 4.706 0 0 0 1.107 1.7c.534.535 1.07.863 1.7 1.108.611.237 1.309.4 2.33.446 1.025.047 1.352.058 3.959.058s2.934-.011 3.958-.058c1.022-.046 1.72-.209 2.33-.446a4.706 4.706 0 0 0 1.7-1.107 4.706 4.706 0 0 0 1.108-1.7c.237-.611.4-1.31.446-2.33.047-1.025.058-1.352.058-3.959s-.011-2.934-.058-3.958c-.047-1.022-.209-1.72-.446-2.33a4.706 4.706 0 0 0-1.107-1.7 4.705 4.705 0 0 0-1.7-1.108c-.611-.237-1.31-.4-2.331-.446C14.934 2.41 14.608 2.4 12 2.4Zm0 1.73c2.563 0 2.867.01 3.88.056.935.042 1.443.199 1.782.33.448.174.768.382 1.104.718.336.336.544.656.718 1.104.131.338.287.847.33 1.783.046 1.012.056 1.316.056 3.879 0 2.563-.01 2.867-.056 3.88-.043.935-.199 1.444-.33 1.782a2.974 2.974 0 0 1-.719 1.104 2.974 2.974 0 0 1-1.103.718c-.339.131-.847.288-1.783.33-1.012.046-1.316.056-3.88.056-2.563 0-2.866-.01-3.878-.056-.936-.042-1.445-.199-1.783-.33a2.974 2.974 0 0 1-1.104-.718 2.974 2.974 0 0 1-.718-1.104c-.131-.338-.288-.847-.33-1.783-.047-1.012-.056-1.316-.056-3.879 0-2.563.01-2.867.056-3.88.042-.935.199-1.443.33-1.782.174-.448.382-.768.718-1.104a2.974 2.974 0 0 1 1.104-.718c.338-.131.847-.288 1.783-.33C9.133 4.14 9.437 4.13 12 4.13Zm0 11.07a3.2 3.2 0 1 1 0-6.4 3.2 3.2 0 0 1 0 6.4Zm0-8.13a4.93 4.93 0 1 0 0 9.86 4.93 4.93 0 0 0 0-9.86Zm6.276-.194a1.152 1.152 0 1 1-2.304 0 1.152 1.152 0 0 1 2.304 0Z"
                            fill="currentColor" />
                    </svg>
                </a>
                <a href="https://www.threads.net/@droppiez.store">
                    <svg aria-hidden="true" focusable="false" width="24" class="icon icon-threads" viewBox="0 0 24 24">
                        <path
                            d="M16.854 10.899a6.682 6.682 0 0 0-.252-.114c-.148-2.731-1.64-4.295-4.146-4.31h-.034c-1.498 0-2.745.64-3.512 1.803l1.378.945c.573-.87 1.473-1.055 2.135-1.055h.023c.825.006 1.447.246 1.85.713.293.34.49.812.587 1.405a10.541 10.541 0 0 0-2.368-.114C10.131 10.31 8.6 11.7 8.704 13.63c.052.98.54 1.822 1.373 2.372.705.465 1.613.693 2.556.641 1.246-.068 2.223-.543 2.905-1.412.518-.66.845-1.516.99-2.593.594.358 1.034.83 1.277 1.396.413.964.437 2.547-.855 3.838-1.132 1.13-2.492 1.62-4.549 1.635-2.28-.017-4.006-.748-5.127-2.174-1.05-1.335-1.593-3.264-1.613-5.732.02-2.468.563-4.397 1.613-5.732C8.395 4.442 10.12 3.711 12.4 3.694c2.298.017 4.053.752 5.217 2.185.571.702 1.002 1.586 1.286 2.616l1.614-.43c-.344-1.269-.885-2.361-1.622-3.268C17.404 2.961 15.22 2.02 12.406 2h-.01c-2.808.02-4.967.964-6.417 2.808C4.689 6.448 4.022 8.732 4 11.593v.014c.022 2.861.688 5.144 1.979 6.785 1.45 1.844 3.61 2.789 6.417 2.808h.01c2.497-.017 4.256-.67 5.706-2.119 1.896-1.894 1.839-4.27 1.214-5.727-.448-1.045-1.303-1.894-2.472-2.455Zm-4.31 4.052c-1.044.058-2.129-.41-2.182-1.414-.04-.744.53-1.574 2.246-1.673a9.52 9.52 0 0 1 .58-.017c.623 0 1.206.06 1.736.176-.198 2.47-1.358 2.872-2.38 2.928Z"
                            fill="currentColor" />
                    </svg>
                </a>
                <a href="https://www.pinterest.com/droppiez/">
                    <svg aria-hidden="true" focusable="false" width="24" class="icon icon-pinterest"
                        viewBox="0 0 24 24">
                        <path fill-rule="evenodd" clip-rule="evenodd"
                            d="M11.765 2.401c3.59-.054 5.837 1.4 6.895 3.95.349.842.722 2.39.442 3.675-.112.512-.144 1.048-.295 1.53-.308.983-.708 1.853-1.238 2.603-.72 1.02-1.81 1.706-3.182 2.052-1.212.305-2.328-.152-2.976-.643-.206-.156-.483-.36-.56-.643h-.029c-.046.515-.244 1.062-.383 1.531-.193.65-.23 1.321-.472 1.929a12.345 12.345 0 0 1-.942 1.868c-.184.302-.692 1.335-1.061 1.347-.04-.078-.057-.108-.06-.245-.118-.19-.035-.508-.087-.766-.082-.4-.145-1.123-.06-1.53v-.643c.096-.442.092-.894.207-1.317.25-.92.39-1.895.648-2.848.249-.915.477-1.916.678-2.847.045-.21-.21-.815-.265-1.041-.174-.713-.042-1.7.176-2.236.275-.674 1.08-1.703 2.122-1.439.838.212 1.371 1.118 1.09 2.266-.295 1.205-.677 2.284-.943 3.49-.068.311.05.641.118.827.248.672 1 1.324 2.004 1.072 1.52-.383 2.193-1.76 2.652-3.246.124-.402.109-.781.206-1.225.204-.935.118-2.331-.177-3.061-.472-1.17-1.353-1.92-2.563-2.328L12.707 4.3c-.56-.128-1.626.064-2.004.183-1.69.535-2.737 1.427-3.388 3.032-.222.546-.344 1.1-.383 1.868l-.03.276c.13.686.144 1.14.413 1.653.132.252.447.451.5.765.032.185-.104.464-.147.613-.065.224-.041.48-.147.673-.192.349-.714.087-.943-.061-1.192-.77-2.175-2.995-1.62-5.144.085-.332.09-.62.206-.919.723-1.844 1.802-2.978 3.359-3.95.583-.364 1.37-.544 2.092-.734l1.149-.154Z"
                            fill="currentColor" />
                    </svg>
                </a>
                <a href="https://www.youtube.com/@droppiez_store">
                    <svg aria-hidden="true" focusable="false" width="24" class="icon icon-youtube" viewBox="0 0 24 24">
                        <path fill-rule="evenodd" clip-rule="evenodd"
                            d="M20.44 5.243c.929.244 1.66.963 1.909 1.876.451 1.654.451 5.106.451 5.106s0 3.452-.451 5.106a2.681 2.681 0 0 1-1.91 1.876c-1.684.443-8.439.443-8.439.443s-6.754 0-8.439-.443a2.682 2.682 0 0 1-1.91-1.876c-.45-1.654-.45-5.106-.45-5.106s0-3.452.45-5.106a2.681 2.681 0 0 1 1.91-1.876c1.685-.443 8.44-.443 8.44-.443s6.754 0 8.438.443Zm-5.004 6.982L9.792 15.36V9.091l5.646 3.134Z"
                            fill="currentColor" />
                    </svg>
                </a>
                <a href="https://www.tiktok.com/@droppeiz">
                    <svg aria-hidden="true" focusable="false" width="24" class="icon icon-tiktok" viewBox="0 0 24 24">
                        <path
                            d="M20.027 10.168a5.125 5.125 0 0 1-4.76-2.294v7.893a5.833 5.833 0 1 1-5.834-5.834c.122 0 .241.011.361.019v2.874c-.12-.014-.237-.036-.36-.036a2.977 2.977 0 0 0 0 5.954c1.644 0 3.096-1.295 3.096-2.94L12.56 2.4h2.75a5.122 5.122 0 0 0 4.72 4.573v3.195"
                            fill="currentColor" />
                    </svg>
                </a>
                <a href="https://vimeo.com/droppiez">
                    <svg aria-hidden="true" focusable="false" width="24" class="icon icon-vimeo" viewBox="0 0 24 24">
                        <path fill-rule="evenodd" clip-rule="evenodd"
                            d="M21.518 6.726c.143-.815.14-1.654-.356-2.288-.693-.89-2.167-.922-3.178-.765-.821.127-3.6 1.371-4.547 4.35 1.676-.13 2.554.122 2.393 1.994-.068.783-.457 1.642-.893 2.464-.502.948-1.445 2.81-2.68 1.468-1.114-1.208-1.03-3.518-1.285-5.056-.142-.864-.292-1.94-.57-2.827-.24-.763-.791-1.684-1.465-1.883-.724-.216-1.618.12-2.143.435C5.12 5.615 3.847 7.034 2.4 8.204v.11c.287.278.364.734.786.796.996.149 1.945-.942 2.607.193.403.693.529 1.453.787 2.2.344.996.61 2.08.892 3.224.477 1.939 1.064 4.836 2.715 5.545.843.363 2.11-.122 2.75-.508 1.738-1.043 3.091-2.555 4.25-4.094 2.649-3.64 4.11-7.765 4.331-8.944Z"
                            fill="currentColor" />
                    </svg>
                </a>
                <a href="https://www.linkedin.com/company/droppiez">
                    <svg aria-hidden="true" focusable="false" width="24" class="icon icon-linkedin" viewBox="0 0 24 24">
                        <path fill-rule="evenodd" clip-rule="evenodd"
                            d="M7.349 5.478a1.875 1.875 0 1 0-3.749 0 1.875 1.875 0 1 0 3.749 0ZM7.092 19.2H3.857V8.78h3.235V19.2ZM12.22 8.78H9.121V19.2h3.228v-5.154c0-1.36.257-2.676 1.94-2.676 1.658 0 1.68 1.554 1.68 2.763V19.2H19.2v-5.715c0-2.806-.605-4.963-3.877-4.963-1.573 0-2.629.863-3.06 1.683h-.044V8.78Z"
                            fill="currentColor" />
                    </svg>
                </a>
                <a href="https://www.snapchat.com/add/droppiez">
                    <svg aria-hidden="true" focusable="false" width="24" class="icon icon-snapchat" viewBox="0 0 24 24">
                        <path fill-rule="evenodd" clip-rule="evenodd"
                            d="M12.121 21.6c-.05 0-.098-.001-.147-.004a1.3 1.3 0 0 1-.096.004c-1.137 0-1.867-.516-2.573-1.014-.488-.344-.947-.669-1.49-.759a4.816 4.816 0 0 0-.782-.066c-.458 0-.82.07-1.083.122-.16.032-.3.059-.404.059-.11 0-.23-.024-.281-.2a6.305 6.305 0 0 1-.109-.445c-.08-.37-.138-.596-.292-.62-1.805-.278-2.32-.657-2.436-.927a.344.344 0 0 1-.028-.115.203.203 0 0 1 .17-.212c2.773-.456 4.017-3.287 4.069-3.407l.004-.01c.17-.343.203-.642.1-.886-.191-.448-.812-.645-1.223-.775-.1-.032-.196-.062-.27-.091-.82-.324-.889-.656-.857-.826.055-.289.441-.49.754-.49a.53.53 0 0 1 .224.045c.369.173.701.26.988.26.396 0 .57-.166.59-.188-.01-.188-.022-.383-.035-.585-.082-1.31-.185-2.937.23-3.866 1.243-2.784 3.88-3 4.658-3l.341-.004h.046c.78 0 3.423.217 4.667 3.002.415.93.312 2.558.23 3.867l-.004.057c-.012.182-.023.36-.032.529.02.02.179.173.538.187.274-.01.587-.098.932-.259a.704.704 0 0 1 .29-.057c.116 0 .234.023.332.064l.006.002c.278.099.46.294.465.497.003.192-.143.48-.863.764-.074.03-.17.06-.27.092-.412.13-1.032.327-1.223.775-.104.244-.07.542.1.886l.004.01c.052.12 1.294 2.95 4.069 3.407a.203.203 0 0 1 .17.212.342.342 0 0 1-.029.116c-.114.267-.63.646-2.435.924-.147.023-.204.215-.292.617-.032.147-.065.29-.11.442-.038.131-.12.193-.258.193h-.022a2.26 2.26 0 0 1-.404-.051 5.394 5.394 0 0 0-1.084-.115c-.254 0-.518.022-.782.066-.542.09-1.001.414-1.488.758-.707.5-1.437 1.015-2.575 1.015Z"
                            fill="currentColor" />
                    </svg>
                </a>
                <a href="https://www.tumblr.com/blog/droppiez">
                    <svg aria-hidden="true" focusable="false" width="24" class="icon icon-tumblr" viewBox="0 0 24 24">
                        <path fill-rule="evenodd" clip-rule="evenodd"
                            d="M13.906 20.4c-2.526 0-4.41-1.3-4.41-4.41v-4.98H7.2V8.314c2.527-.657 3.584-2.83 3.706-4.714h2.623v4.277h3.061v3.133h-3.06v4.337c0 1.3.655 1.75 1.7 1.75h1.482V20.4h-2.806Z"
                            fill="currentColor" />
                    </svg>
                </a>
                <a href="https://www.reddit.com/user/droppiez/">
                    <svg aria-hidden="true" focusable="false" width="24" class="icon icon-reddit" viewBox="0 0 24 24">
                        <path
                            d="M21.604 10.841c.243.347.38.756.396 1.178a2.192 2.192 0 0 1-1.216 1.997c.017.22.017.441 0 .66 0 3.364-3.92 6.097-8.754 6.097s-8.753-2.733-8.753-6.096a4.307 4.307 0 0 1 0-.66 2.193 2.193 0 1 1 2.417-3.59 10.72 10.72 0 0 1 5.856-1.846l1.11-5.21a.465.465 0 0 1 .556-.36l3.679.736a1.501 1.501 0 1 1-.195.915l-3.213-.675-.976 4.684a10.69 10.69 0 0 1 5.78 1.847 2.192 2.192 0 0 1 3.313.323Z"
                            fill="currentColor" />
                    </svg>
                </a>
            </div>
            <div class="columns-2">
                <div class="text-center">
                    <p class="copyright-text">&copy; 2024 - Droppiez LLC. All Rights Reserved.</p>
                </div>
                <div class="payment-icons inline-grid grid-cols-9 gap-4">
                    <svg xmlns="http://www.w3.org/2000/svg" role="img" aria-labelledby="pi-american_express"
                        viewBox="0 0 38 24" width="38" height="24">
                        <title id="pi-american_express">American Express</title>
                        <path fill="#000"
                            d="M35 0H3C1.3 0 0 1.3 0 3v18c0 1.7 1.4 3 3 3h32c1.7 0 3-1.3 3-3V3c0-1.7-1.4-3-3-3Z"
                            opacity=".07" />
                        <path fill="#006FCF"
                            d="M35 1c1.1 0 2 .9 2 2v18c0 1.1-.9 2-2 2H3c-1.1 0-2-.9-2-2V3c0-1.1.9-2 2-2h32Z" />
                        <path fill="#FFF"
                            d="M22.012 19.936v-8.421L37 11.528v2.326l-1.732 1.852L37 17.573v2.375h-2.766l-1.47-1.622-1.46 1.628-9.292-.02Z" />
                        <path fill="#006FCF"
                            d="M23.013 19.012v-6.57h5.572v1.513h-3.768v1.028h3.678v1.488h-3.678v1.01h3.768v1.531h-5.572Z" />
                        <path fill="#006FCF"
                            d="m28.557 19.012 3.083-3.289-3.083-3.282h2.386l1.884 2.083 1.89-2.082H37v.051l-3.017 3.23L37 18.92v.093h-2.307l-1.917-2.103-1.898 2.104h-2.321Z" />
                        <path fill="#FFF"
                            d="M22.71 4.04h3.614l1.269 2.881V4.04h4.46l.77 2.159.771-2.159H37v8.421H19l3.71-8.421Z" />
                        <path fill="#006FCF"
                            d="m23.395 4.955-2.916 6.566h2l.55-1.315h2.98l.55 1.315h2.05l-2.904-6.566h-2.31Zm.25 3.777.875-2.09.873 2.09h-1.748Z" />
                        <path fill="#006FCF"
                            d="M28.581 11.52V4.953l2.811.01L32.84 9l1.456-4.046H37v6.565l-1.74.016v-4.51l-1.644 4.494h-1.59L30.35 7.01v4.51h-1.768Z" />
                    </svg>
                    <svg version="1.1" xmlns="http://www.w3.org/2000/svg" role="img" x="0" y="0" width="38" height="24"
                        viewBox="0 0 165.521 105.965" xml:space="preserve" aria-labelledby="pi-apple_pay">
                        <title id="pi-apple_pay">Apple Pay</title>
                        <path fill="#000"
                            d="M150.698 0H14.823c-.566 0-1.133 0-1.698.003-.477.004-.953.009-1.43.022-1.039.028-2.087.09-3.113.274a10.51 10.51 0 0 0-2.958.975 9.932 9.932 0 0 0-4.35 4.35 10.463 10.463 0 0 0-.975 2.96C.113 9.611.052 10.658.024 11.696a70.22 70.22 0 0 0-.022 1.43C0 13.69 0 14.256 0 14.823v76.318c0 .567 0 1.132.002 1.699.003.476.009.953.022 1.43.028 1.036.09 2.084.275 3.11a10.46 10.46 0 0 0 .974 2.96 9.897 9.897 0 0 0 1.83 2.52 9.874 9.874 0 0 0 2.52 1.83c.947.483 1.917.79 2.96.977 1.025.183 2.073.245 3.112.273.477.011.953.017 1.43.02.565.004 1.132.004 1.698.004h135.875c.565 0 1.132 0 1.697-.004.476-.002.952-.009 1.431-.02 1.037-.028 2.085-.09 3.113-.273a10.478 10.478 0 0 0 2.958-.977 9.955 9.955 0 0 0 4.35-4.35c.483-.947.789-1.917.974-2.96.186-1.026.246-2.074.274-3.11.013-.477.02-.954.022-1.43.004-.567.004-1.132.004-1.699V14.824c0-.567 0-1.133-.004-1.699a63.067 63.067 0 0 0-.022-1.429c-.028-1.038-.088-2.085-.274-3.112a10.4 10.4 0 0 0-.974-2.96 9.94 9.94 0 0 0-4.35-4.35A10.52 10.52 0 0 0 156.939.3c-1.028-.185-2.076-.246-3.113-.274a71.417 71.417 0 0 0-1.431-.022C151.83 0 151.263 0 150.698 0z" />
                        <path fill="#FFF"
                            d="M150.698 3.532l1.672.003c.452.003.905.008 1.36.02.793.022 1.719.065 2.583.22.75.135 1.38.34 1.984.648a6.392 6.392 0 0 1 2.804 2.807c.306.6.51 1.226.645 1.983.154.854.197 1.783.218 2.58.013.45.019.9.02 1.36.005.557.005 1.113.005 1.671v76.318c0 .558 0 1.114-.004 1.682-.002.45-.008.9-.02 1.35-.022.796-.065 1.725-.221 2.589a6.855 6.855 0 0 1-.645 1.975 6.397 6.397 0 0 1-2.808 2.807c-.6.306-1.228.511-1.971.645-.881.157-1.847.2-2.574.22-.457.01-.912.017-1.379.019-.555.004-1.113.004-1.669.004H14.801c-.55 0-1.1 0-1.66-.004a74.993 74.993 0 0 1-1.35-.018c-.744-.02-1.71-.064-2.584-.22a6.938 6.938 0 0 1-1.986-.65 6.337 6.337 0 0 1-1.622-1.18 6.355 6.355 0 0 1-1.178-1.623 6.935 6.935 0 0 1-.646-1.985c-.156-.863-.2-1.788-.22-2.578a66.088 66.088 0 0 1-.02-1.355l-.003-1.327V14.474l.002-1.325a66.7 66.7 0 0 1 .02-1.357c.022-.792.065-1.717.222-2.587a6.924 6.924 0 0 1 .646-1.981c.304-.598.7-1.144 1.18-1.623a6.386 6.386 0 0 1 1.624-1.18 6.96 6.96 0 0 1 1.98-.646c.865-.155 1.792-.198 2.586-.22.452-.012.905-.017 1.354-.02l1.677-.003h135.875" />
                        <g>
                            <g>
                                <path fill="#000"
                                    d="M43.508 35.77c1.404-1.755 2.356-4.112 2.105-6.52-2.054.102-4.56 1.355-6.012 3.112-1.303 1.504-2.456 3.959-2.156 6.266 2.306.2 4.61-1.152 6.063-2.858" />
                                <path fill="#000"
                                    d="M45.587 39.079c-3.35-.2-6.196 1.9-7.795 1.9-1.6 0-4.049-1.8-6.698-1.751-3.447.05-6.645 2-8.395 5.1-3.598 6.2-.95 15.4 2.55 20.45 1.699 2.5 3.747 5.25 6.445 5.151 2.55-.1 3.549-1.65 6.647-1.65 3.097 0 3.997 1.65 6.696 1.6 2.798-.05 4.548-2.5 6.247-5 1.95-2.85 2.747-5.6 2.797-5.75-.05-.05-5.396-2.101-5.446-8.251-.05-5.15 4.198-7.6 4.398-7.751-2.399-3.548-6.147-3.948-7.447-4.048" />
                            </g>
                            <g>
                                <path fill="#000"
                                    d="M78.973 32.11c7.278 0 12.347 5.017 12.347 12.321 0 7.33-5.173 12.373-12.529 12.373h-8.058V69.62h-5.822V32.11h14.062zm-8.24 19.807h6.68c5.07 0 7.954-2.729 7.954-7.46 0-4.73-2.885-7.434-7.928-7.434h-6.706v14.894z" />
                                <path fill="#000"
                                    d="M92.764 61.847c0-4.809 3.665-7.564 10.423-7.98l7.252-.442v-2.08c0-3.04-2.001-4.704-5.562-4.704-2.938 0-5.07 1.507-5.51 3.82h-5.252c.157-4.86 4.731-8.395 10.918-8.395 6.654 0 10.995 3.483 10.995 8.89v18.663h-5.38v-4.497h-.13c-1.534 2.937-4.914 4.782-8.579 4.782-5.406 0-9.175-3.222-9.175-8.057zm17.675-2.417v-2.106l-6.472.416c-3.64.234-5.536 1.585-5.536 3.95 0 2.288 1.975 3.77 5.068 3.77 3.95 0 6.94-2.522 6.94-6.03z" />
                                <path fill="#000"
                                    d="M120.975 79.652v-4.496c.364.051 1.247.103 1.715.103 2.573 0 4.029-1.09 4.913-3.899l.52-1.663-9.852-27.293h6.082l6.863 22.146h.13l6.862-22.146h5.927l-10.216 28.67c-2.34 6.577-5.017 8.735-10.683 8.735-.442 0-1.872-.052-2.261-.157z" />
                            </g>
                        </g>
                    </svg>
                    <svg viewBox="0 0 38 24" xmlns="http://www.w3.org/2000/svg" role="img" width="38" height="24"
                        aria-labelledby="pi-diners_club">
                        <title id="pi-diners_club">Diners Club</title>
                        <path opacity=".07"
                            d="M35 0H3C1.3 0 0 1.3 0 3v18c0 1.7 1.4 3 3 3h32c1.7 0 3-1.3 3-3V3c0-1.7-1.4-3-3-3z" />
                        <path fill="#fff"
                            d="M35 1c1.1 0 2 .9 2 2v18c0 1.1-.9 2-2 2H3c-1.1 0-2-.9-2-2V3c0-1.1.9-2 2-2h32" />
                        <path
                            d="M12 12v3.7c0 .3-.2.3-.5.2-1.9-.8-3-3.3-2.3-5.4.4-1.1 1.2-2 2.3-2.4.4-.2.5-.1.5.2V12zm2 0V8.3c0-.3 0-.3.3-.2 2.1.8 3.2 3.3 2.4 5.4-.4 1.1-1.2 2-2.3 2.4-.4.2-.4.1-.4-.2V12zm7.2-7H13c3.8 0 6.8 3.1 6.8 7s-3 7-6.8 7h8.2c3.8 0 6.8-3.1 6.8-7s-3-7-6.8-7z"
                            fill="#3086C8" />
                    </svg>
                    <svg viewBox="0 0 38 24" width="38" height="24" role="img" aria-labelledby="pi-discover" fill="none"
                        xmlns="http://www.w3.org/2000/svg">
                        <title id="pi-discover">Discover</title>
                        <path fill="#000" opacity=".07"
                            d="M35 0H3C1.3 0 0 1.3 0 3v18c0 1.7 1.4 3 3 3h32c1.7 0 3-1.3 3-3V3c0-1.7-1.4-3-3-3z" />
                        <path d="M35 1c1.1 0 2 .9 2 2v18c0 1.1-.9 2-2 2H3c-1.1 0-2-.9-2-2V3c0-1.1.9-2 2-2h32z"
                            fill="#fff" />
                        <path
                            d="M3.57 7.16H2v5.5h1.57c.83 0 1.43-.2 1.96-.63.63-.52 1-1.3 1-2.11-.01-1.63-1.22-2.76-2.96-2.76zm1.26 4.14c-.34.3-.77.44-1.47.44h-.29V8.1h.29c.69 0 1.11.12 1.47.44.37.33.59.84.59 1.37 0 .53-.22 1.06-.59 1.39zm2.19-4.14h1.07v5.5H7.02v-5.5zm3.69 2.11c-.64-.24-.83-.4-.83-.69 0-.35.34-.61.8-.61.32 0 .59.13.86.45l.56-.73c-.46-.4-1.01-.61-1.62-.61-.97 0-1.72.68-1.72 1.58 0 .76.35 1.15 1.35 1.51.42.15.63.25.74.31.21.14.32.34.32.57 0 .45-.35.78-.83.78-.51 0-.92-.26-1.17-.73l-.69.67c.49.73 1.09 1.05 1.9 1.05 1.11 0 1.9-.74 1.9-1.81.02-.89-.35-1.29-1.57-1.74zm1.92.65c0 1.62 1.27 2.87 2.9 2.87.46 0 .86-.09 1.34-.32v-1.26c-.43.43-.81.6-1.29.6-1.08 0-1.85-.78-1.85-1.9 0-1.06.79-1.89 1.8-1.89.51 0 .9.18 1.34.62V7.38c-.47-.24-.86-.34-1.32-.34-1.61 0-2.92 1.28-2.92 2.88zm12.76.94l-1.47-3.7h-1.17l2.33 5.64h.58l2.37-5.64h-1.16l-1.48 3.7zm3.13 1.8h3.04v-.93h-1.97v-1.48h1.9v-.93h-1.9V8.1h1.97v-.94h-3.04v5.5zm7.29-3.87c0-1.03-.71-1.62-1.95-1.62h-1.59v5.5h1.07v-2.21h.14l1.48 2.21h1.32l-1.73-2.32c.81-.17 1.26-.72 1.26-1.56zm-2.16.91h-.31V8.03h.33c.67 0 1.03.28 1.03.82 0 .55-.36.85-1.05.85z"
                            fill="#231F20" />
                        <path d="M20.16 12.86a2.931 2.931 0 100-5.862 2.931 2.931 0 000 5.862z"
                            fill="url(#pi-paint0_linear)" />
                        <path opacity=".65" d="M20.16 12.86a2.931 2.931 0 100-5.862 2.931 2.931 0 000 5.862z"
                            fill="url(#pi-paint1_linear)" />
                        <path
                            d="M36.57 7.506c0-.1-.07-.15-.18-.15h-.16v.48h.12v-.19l.14.19h.14l-.16-.2c.06-.01.1-.06.1-.13zm-.2.07h-.02v-.13h.02c.06 0 .09.02.09.06 0 .05-.03.07-.09.07z"
                            fill="#231F20" />
                        <path
                            d="M36.41 7.176c-.23 0-.42.19-.42.42 0 .23.19.42.42.42.23 0 .42-.19.42-.42 0-.23-.19-.42-.42-.42zm0 .77c-.18 0-.34-.15-.34-.35 0-.19.15-.35.34-.35.18 0 .33.16.33.35 0 .19-.15.35-.33.35z"
                            fill="#231F20" />
                        <path d="M37 12.984S27.09 19.873 8.976 23h26.023a2 2 0 002-1.984l.024-3.02L37 12.985z"
                            fill="#F48120" />
                        <defs>
                            <linearGradient id="pi-paint0_linear" x1="21.657" y1="12.275" x2="19.632" y2="9.104"
                                gradientUnits="userSpaceOnUse">
                                <stop stop-color="#F89F20" />
                                <stop offset=".25" stop-color="#F79A20" />
                                <stop offset=".533" stop-color="#F68D20" />
                                <stop offset=".62" stop-color="#F58720" />
                                <stop offset=".723" stop-color="#F48120" />
                                <stop offset="1" stop-color="#F37521" />
                            </linearGradient>
                            <linearGradient id="pi-paint1_linear" x1="21.338" y1="12.232" x2="18.378" y2="6.446"
                                gradientUnits="userSpaceOnUse">
                                <stop stop-color="#F58720" />
                                <stop offset=".359" stop-color="#E16F27" />
                                <stop offset=".703" stop-color="#D4602C" />
                                <stop offset=".982" stop-color="#D05B2E" />
                            </linearGradient>
                        </defs>
                    </svg>
                    <svg width="38" height="24" role="img" aria-labelledby="pi-jcb" viewBox="0 0 38 24"
                        xmlns="http://www.w3.org/2000/svg">
                        <title id="pi-jcb">JCB</title>
                        <g fill="none" fill-rule="evenodd">
                            <g fill-rule="nonzero">
                                <path
                                    d="M35 0H3C1.3 0 0 1.3 0 3v18c0 1.7 1.4 3 3 3h32c1.7 0 3-1.3 3-3V3c0-1.7-1.4-3-3-3z"
                                    fill="#000" opacity=".07" />
                                <path d="M35 1c1.1 0 2 .9 2 2v18c0 1.1-.9 2-2 2H3c-1.1 0-2-.9-2-2V3c0-1.1.9-2 2-2h32"
                                    fill="#FFF" />
                            </g>
                            <path d="M11.5 5H15v11.5a2.5 2.5 0 0 1-2.5 2.5H9V7.5A2.5 2.5 0 0 1 11.5 5z"
                                fill="#006EBC" />
                            <path d="M18.5 5H22v11.5a2.5 2.5 0 0 1-2.5 2.5H16V7.5A2.5 2.5 0 0 1 18.5 5z"
                                fill="#F00036" />
                            <path d="M25.5 5H29v11.5a2.5 2.5 0 0 1-2.5 2.5H23V7.5A2.5 2.5 0 0 1 25.5 5z"
                                fill="#2AB419" />
                            <path
                                d="M10.755 14.5c-1.06 0-2.122-.304-2.656-.987l.78-.676c.068 1.133 3.545 1.24 3.545-.19V9.5h1.802v3.147c0 .728-.574 1.322-1.573 1.632-.466.144-1.365.221-1.898.221zm8.116 0c-.674 0-1.388-.107-1.965-.366-.948-.425-1.312-1.206-1.3-2.199.012-1.014.436-1.782 1.468-2.165 1.319-.49 3.343-.261 3.926.27v.972c-.572-.521-1.958-.898-2.919-.46-.494.226-.737.917-.744 1.448-.006.56.245 1.252.744 1.497.953.467 2.39.04 2.919-.441v1.01c-.358.255-1.253.434-2.129.434zm8.679-2.587c.37-.235.582-.567.582-1.005 0-.438-.116-.687-.348-.939-.206-.207-.58-.469-1.238-.469H23v5h3.546c.696 0 1.097-.23 1.315-.415.283-.25.426-.53.426-.96 0-.431-.155-.908-.737-1.212zm-1.906-.281h-1.428v-1.444h1.495c.956 0 .944 1.444-.067 1.444zm.288 2.157h-1.716v-1.513h1.716c.986 0 1.083 1.513 0 1.513z"
                                fill="#FFF" fill-rule="nonzero" />
                        </g>
                    </svg>
                    <svg viewBox="0 0 38 24" xmlns="http://www.w3.org/2000/svg" role="img" width="38" height="24"
                        aria-labelledby="pi-master">
                        <title id="pi-master">Mastercard</title>
                        <path opacity=".07"
                            d="M35 0H3C1.3 0 0 1.3 0 3v18c0 1.7 1.4 3 3 3h32c1.7 0 3-1.3 3-3V3c0-1.7-1.4-3-3-3z" />
                        <path fill="#fff"
                            d="M35 1c1.1 0 2 .9 2 2v18c0 1.1-.9 2-2 2H3c-1.1 0-2-.9-2-2V3c0-1.1.9-2 2-2h32" />
                        <circle fill="#EB001B" cx="15" cy="12" r="7" />
                        <circle fill="#F79E1B" cx="23" cy="12" r="7" />
                        <path fill="#FF5F00"
                            d="M22 12c0-2.4-1.2-4.5-3-5.7-1.8 1.3-3 3.4-3 5.7s1.2 4.5 3 5.7c1.8-1.2 3-3.3 3-5.7z" />
                    </svg>
                    <svg viewBox="0 0 38 24" xmlns="http://www.w3.org/2000/svg" width="38" height="24" role="img"
                        aria-labelledby="pi-paypal">
                        <title id="pi-paypal">PayPal</title>
                        <path opacity=".07"
                            d="M35 0H3C1.3 0 0 1.3 0 3v18c0 1.7 1.4 3 3 3h32c1.7 0 3-1.3 3-3V3c0-1.7-1.4-3-3-3z" />
                        <path fill="#fff"
                            d="M35 1c1.1 0 2 .9 2 2v18c0 1.1-.9 2-2 2H3c-1.1 0-2-.9-2-2V3c0-1.1.9-2 2-2h32" />
                        <path fill="#003087"
                            d="M23.9 8.3c.2-1 0-1.7-.6-2.3-.6-.7-1.7-1-3.1-1h-4.1c-.3 0-.5.2-.6.5L14 15.6c0 .2.1.4.3.4H17l.4-3.4 1.8-2.2 4.7-2.1z" />
                        <path fill="#3086C8"
                            d="M23.9 8.3l-.2.2c-.5 2.8-2.2 3.8-4.6 3.8H18c-.3 0-.5.2-.6.5l-.6 3.9-.2 1c0 .2.1.4.3.4H19c.3 0 .5-.2.5-.4v-.1l.4-2.4v-.1c0-.2.3-.4.5-.4h.3c2.1 0 3.7-.8 4.1-3.2.2-1 .1-1.8-.4-2.4-.1-.5-.3-.7-.5-.8z" />
                        <path fill="#012169"
                            d="M23.3 8.1c-.1-.1-.2-.1-.3-.1-.1 0-.2 0-.3-.1-.3-.1-.7-.1-1.1-.1h-3c-.1 0-.2 0-.2.1-.2.1-.3.2-.3.4l-.7 4.4v.1c0-.3.3-.5.6-.5h1.3c2.5 0 4.1-1 4.6-3.8v-.2c-.1-.1-.3-.2-.5-.2h-.1z" />
                    </svg>
                    <svg viewBox="0 0 38 24" width="38" height="24" xmlns="http://www.w3.org/2000/svg" role="img"
                        aria-labelledby="pi-venmo">
                        <title id="pi-venmo">Venmo</title>
                        <g fill="none" fill-rule="evenodd">
                            <rect fill-opacity=".07" fill="#000" width="38" height="24" rx="3" />
                            <path fill="#3D95CE"
                                d="M35 1c1.1 0 2 .9 2 2v18c0 1.1-.9 2-2 2H3c-1.1 0-2-.9-2-2V3c0-1.1.9-2 2-2h32" />
                            <path
                                d="M24.675 8.36c0 3.064-2.557 7.045-4.633 9.84h-4.74L13.4 6.57l4.151-.402 1.005 8.275c.94-1.566 2.099-4.025 2.099-5.702 0-.918-.154-1.543-.394-2.058l3.78-.783c.437.738.634 1.499.634 2.46z"
                                fill="#FFF" fill-rule="nonzero" />
                        </g>
                    </svg>
                    <svg viewBox="0 0 38 24" xmlns="http://www.w3.org/2000/svg" role="img" width="38" height="24"
                        aria-labelledby="pi-visa">
                        <title id="pi-visa">Visa</title>
                        <path opacity=".07"
                            d="M35 0H3C1.3 0 0 1.3 0 3v18c0 1.7 1.4 3 3 3h32c1.7 0 3-1.3 3-3V3c0-1.7-1.4-3-3-3z" />
                        <path fill="#fff"
                            d="M35 1c1.1 0 2 .9 2 2v18c0 1.1-.9 2-2 2H3c-1.1 0-2-.9-2-2V3c0-1.1.9-2 2-2h32" />
                        <path
                            d="M28.3 10.1H28c-.4 1-.7 1.5-1 3h1.9c-.3-1.5-.3-2.2-.6-3zm2.9 5.9h-1.7c-.1 0-.1 0-.2-.1l-.2-.9-.1-.2h-2.4c-.1 0-.2 0-.2.2l-.3.9c0 .1-.1.1-.1.1h-2.1l.2-.5L27 8.7c0-.5.3-.7.8-.7h1.5c.1 0 .2 0 .2.2l1.4 6.5c.1.4.2.7.2 1.1.1.1.1.1.1.2zm-13.4-.3l.4-1.8c.1 0 .2.1.2.1.7.3 1.4.5 2.1.4.2 0 .5-.1.7-.2.5-.2.5-.7.1-1.1-.2-.2-.5-.3-.8-.5-.4-.2-.8-.4-1.1-.7-1.2-1-.8-2.4-.1-3.1.6-.4.9-.8 1.7-.8 1.2 0 2.5 0 3.1.2h.1c-.1.6-.2 1.1-.4 1.7-.5-.2-1-.4-1.5-.4-.3 0-.6 0-.9.1-.2 0-.3.1-.4.2-.2.2-.2.5 0 .7l.5.4c.4.2.8.4 1.1.6.5.3 1 .8 1.1 1.4.2.9-.1 1.7-.9 2.3-.5.4-.7.6-1.4.6-1.4 0-2.5.1-3.4-.2-.1.2-.1.2-.2.1zm-3.5.3c.1-.7.1-.7.2-1 .5-2.2 1-4.5 1.4-6.7.1-.2.1-.3.3-.3H18c-.2 1.2-.4 2.1-.7 3.2-.3 1.5-.6 3-1 4.5 0 .2-.1.2-.3.2M5 8.2c0-.1.2-.2.3-.2h3.4c.5 0 .9.3 1 .8l.9 4.4c0 .1 0 .1.1.2 0-.1.1-.1.1-.1l2.1-5.1c-.1-.1 0-.2.1-.2h2.1c0 .1 0 .1-.1.2l-3.1 7.3c-.1.2-.1.3-.2.4-.1.1-.3 0-.5 0H9.7c-.1 0-.2 0-.2-.2L7.9 9.5c-.2-.2-.5-.5-.9-.6-.6-.3-1.7-.5-1.9-.5L5 8.2z"
                            fill="#142688" />
                    </svg>
                </div>
            </div>
        </div>
    </footer>
</template>

<style>
.footer {
    background-color: #f9f9f9;
    color: #282828;
    font-family: Arial, sans-serif;
    padding: 30px 0;
}

.footer-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    max-width: 1200px;
    margin: 0 auto;
}

.footer-column {
    flex: 0 1 22%;
    margin: 10px;
}

.footer-column p {
    font-size: 14px;
}

.footer-column h4 {
    font-size: 16px;
    margin-bottom: 10px;
    text-transform: uppercase;
    font-weight: 900;
}

.footer-column ul {
    list-style: none;
    padding: 0;
}

.footer-column ul li a {
    text-decoration: underline;
    color: #282828;
    font-size: 14px;
    transition: all 0.3s ease;
}

.footer-column ul li a:hover {
    text-decoration: none;

}

.footer-column address {
    font-style: normal;
    font-size: 14px;
    margin-top: 10px;
}

.footer-column form {
    margin-top: 10px;
}

.footer-column form input {
    padding: 8px;
    border: 1px solid #ddd;
    background: transparent;
    width: 100%;
}

.footer-column form input::placeholder {
    font-size: 14px;
}

.footer-column form button {
    padding: 10px 32px;
    border: none;
    background-color: #282828;
    color: #fff;
    cursor: pointer;
    font-size: 14px;
    letter-spacing: 2px;
}

.footer-column form button:hover {
    background-color: #282828;
}

.copyright-text {
    letter-spacing: 2px;
    font-size: 14px;
    text-align: center;
}

.footer-bottom {
    max-width: 1200px;
    margin: 0 auto;
}
</style>