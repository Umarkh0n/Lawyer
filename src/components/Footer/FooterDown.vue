<script setup>
import Buttons from '../Common/Buttons.vue';
import Navbar from '../navbar/Navbar.vue';

function scrollToTop() {
    window.scrollTo({
        top: 0,
        behavior: 'smooth',
    });
}


</script>

<template>
    <div class="baground_img">
        <div class="containerr">
            <button class="mx-auto block py-6 text-[#cca876;] text-xs" @click="scrollToTop">
                – ↑ BACK TO TOP –
            </button>
            <Navbar :is-hamburger="false" :show-logo="false" class="!justify-center !text-white custom-ul-class" />
            <div class="lg:grid grid-cols-12 mt-16 items-center gap-6 ">
                <div class="col-span-6 lg:flex items-center ">
                    <div class="min-w-[290px] mt-6 lg:mt-0">
                        <h4 class="text-white text-base">
                            London
                        </h4>
                        <h2 class="text-2xl text-[#CCA876]">
                            714.783.2205
                        </h2>
                    </div>
                    <div class="min-w-[290px] mt-6 lg:mt-0">
                        <h4 class="text-white text-base">
                            Tokio
                        </h4>
                        <h2 class="text-2xl text-[#CCA876]">
                            714.783.2205
                        </h2>
                    </div>
                </div>
                <div class="col-span-6 mt-6 lg:mt-0">
                    <Buttons text="REQUEST A FREE CONSULTATION  →" variant="modest" :show-icon="true"
                        icon-class="ri-chat-3-line text-2xl text-[#CCA876] group-hover:text-white" />
                </div>

            </div>
            <div class="lg:grid grid-cols-12 mt-16 items-start gap-6">
                <div class="col-span-6 lg:flex items-start mb-[30px]">
                    <div class="min-w-[290px] mb-5 lg:mb-0">
                        <div class="max-w-[700px] lg:max-w-[255px]">
                            <h4 class="text-white text-xl">
                                About
                            </h4>
                            <p class="my-6 text-xs text-white leading-5 ">
                                Class is also likely to be focused on slow and gentle movements so it's a great type of
                                yoga to is also likely to be focused on slow and gentle movements so it's a great type
                                of yoga to...
                            </p>
                            <Buttons text="Buy This Beatiful Theme" variant="unusual" class="!py-2" />
                        </div>
                    </div>
                    <div class="min-w-[290px]">
                        <div class="max-w-[255px]">
                            <h4 class="text-white text-xl">
                                Practice Areas
                            </h4>
                            <ul class="mt-6 text-sm text-white flex flex-col justify-between min-h-[]">
                                <li class="mb-2">
                                    <RouterLink to="#" class="hover:text-white text-[#cca876;] transition-all">
                                        SERIOUS CAR CRASH →

                                    </RouterLink>
                                </li>
                                <li class="mb-2">
                                    <RouterLink to="#" class="hover:text-white text-[#cca876;] transition-all">
                                        BRAIN INJURY →

                                    </RouterLink>
                                </li>
                                <li class="mb-2">
                                    <RouterLink to="#" class="hover:text-white text-[#cca876;] transition-all">
                                        TRUCK ACCIDENTS →

                                    </RouterLink>
                                </li>
                                <li class="mb-2">
                                    <RouterLink to="#" class="hover:text-white text-[#cca876;] transition-all">
                                        SEMI-TRUCK COLLISION →

                                    </RouterLink>
                                </li>
                                <li class="mb-2">
                                    <RouterLink to="#" class="hover:text-white text-[#cca876;] transition-all">
                                        MOTORCYCLE ACCIDENTS →

                                    </RouterLink>
                                </li>
                                <li class="mb-2">
                                    <RouterLink to="#" class="hover:text-white text-[#cca876;] transition-all">
                                        WRONGFUL DEATH →

                                    </RouterLink>
                                </li>
                            </ul>

                        </div>
                    </div>
                </div>
                <div class="col-span-6 lg:flex items-start mb-[30px]">
                    <div>
                        <div class="min-w-[290px] mb-10 lg:mb-0">
                            <div class="max-w-[255px]">
                                <h4 class="text-white text-xl">
                                    London, UK
                                </h4>
                                <p class="mt-6 text-xs text-white leading-5">
                                    10, Firs Avenue, Muswell Hill,
                                </p>
                                <div class="my-2 text-xs text-white leading-5">
                                    <p>
                                        Tel: 02 562-958
                                    </p>
                                    <p>
                                        Mobile: 02 562-95
                                    </p>
                                    <p class="">
                                        E-mail: <RouterLink class="hover:text-white text-[#cca876] transition-all"
                                            to="#">hello@lawyers.com</RouterLink>
                                    </p>
                                </div>
                                <RouterLink class="text-xs text-[#cca876] hover:text-white transition-all ">
                                    Get directions on the map <span class="text-white">→</span>
                                </RouterLink>

                            </div>
                        </div>
                    </div>
                    <div class="pb-10 lg:pb-0">
                        <div class="min-w-[290px] ">
                            <div class="max-w-[255px]">
                                <h4 class="text-white text-xl">
                                    London, UK
                                </h4>
                                <p class="mt-6 text-xs text-white leading-5">
                                    10, Firs Avenue, Muswell Hill,
                                </p>
                                <div class="my-2 text-xs text-white leading-5">
                                    <p>
                                        Tel: 02 562-958
                                    </p>
                                    <p>
                                        Mobile: 02 562-95
                                    </p>
                                    <p class="">
                                        E-mail: <RouterLink class="hover:text-white text-[#cca876] transition-all"
                                            to="#">hello@lawyers.com</RouterLink>
                                    </p>
                                </div>
                                <RouterLink class="text-xs text-[#cca876] hover:text-white transition-all ">
                                    Get directions on the map <span class="text-white">→</span>
                                </RouterLink>

                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>

<style scoped>
.baground_img {
    background-image: url("https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/09/bg_3.jpg");
    background-size: cover;
    background-repeat: no-repeat;
}

.custom-ul-class ul {
    gap: 10px !important;
}
</style>