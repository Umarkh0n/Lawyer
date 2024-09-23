<script setup>
import Buttons from '@/components/Common/Buttons.vue';

const services = [
    {
        id: 1, image: "https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/09/icon-1.png", title: "Family Law", desc: "Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium lectorum.", link: "Read more →"
    },
    {
        id: 2, image: "https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/09/icon-2.png", title: "Business Law", desc: "Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium lectorum.", link: "Read more →"
    },
    {
        id: 3, image: "https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/09/icon-3.png", title: "Trust & Estates", desc: "Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium lectorum.", link: "Read more →"
    },
    {
        id: 4, image: "https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/09/icon-4.png", title: "Civil Litigation", desc: "Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium lectorum.", link: "Read more →"
    },
]
</script>

<template>
    <section>
        <div class="bg-[url('/public/images/city.webp')] min-h-[600px] bg-cover ">
            <div class="containerr flex items-center justify-between ">
                <div class="text-black uppercase max-w-[500px] mt-48 lg:mt-0">
                    <p class="text-base">
                        with lawyer & attoney
                    </p>
                    <h2 class="text-5xl my-5 text-white md:text-black">
                        meet us & we can help you
                    </h2>
                    <Buttons variant="simpler" text="request a free consultation" />
                </div>
                <div>
                    <img class="lg:block hidden relative z-10"
                        src="https://lawyers-attorneys.vamtam.com/wp-content/uploads/revslider/Home-Slider/slider-home1.png"
                        alt="">
                </div>
            </div>
        </div>
        <!--  -->
        <div
            class=" xl:border border-[#ededed]  relative z-40 xl:!mt-[-60px] !bg-white containerr block xl:flex items-center justify-between !py-5 px-4">
            <div class="min-w-[262px] text-center mt-5 xl:mt-0">
                <div class=" my-3 text-xl font-sans font-bold ">
                    1700+
                    
                </div>
                <h5 class="uppercase text-xs my-3 text-[#cca876]">
                    TRUSTED CLIENTS
                </h5>
            </div>
            <span class="hidden xl:block border h-[50px] "></span>
            <div class="min-w-[262px] text-center mt-5 xl:mt-0">
                <h2 class=" my-3 text-xl font-sans font-bold">
                    $180 000 000
                </h2>
                <h5 class="uppercase text-xs my-3 text-[#cca876]">
                    RECOVERED FOR OUR CLIENTS
                </h5>
            </div>
            <span class="hidden xl:block border h-[50px] "></span>
            <div class="min-w-[262px] text-center mt-5 xl:mt-0">
                <h2 class=" my-3 text-xl font-sans font-bold">
                    98%
                </h2>
                <h5 class="uppercase text-xs my-3 text-[#cca876]">
                    SUCCESSFUL CASES
                </h5>
            </div>
            <span class="hidden xl:block border h-[50px] "></span>
            <div class="min-w-[262px] text-center mt-5 xl:mt-0">
                <h2 class=" my-3 text-xl font-sans font-bold">
                    10,600
                </h2>
                <h5 class="uppercase text-xs my-3 text-[#cca876]">
                    PERSONAL INJURY CASES
                </h5>
            </div>
        </div>
        <!--  -->
        <div class=" block lg:flex items-center justify-between containerr gap-[30px] !mt-[50px]">
            <div v-for="service in services">
                <RouterLink to="/" class="group">
                    <div class="py-5">
                        <img :src="service.image" alt="">
                    </div>
                    <span class="block w-full border group-hover:border-[#9b7b4d] transition"></span>
                    <span class="block w-full border mt-[2px] group-hover:border-[#9b7b4d] transition"></span>
                    <div class="font-sans">
                        <h3 class="group-hover:text-[#9b7b4d] transition mt-5 ">
                            {{ service.title }}
                        </h3>
                        <p class="mt-5 text-sm ">
                            {{ service.desc }}
                        </p>
                        <p class="text-[#551a8b] group-hover:text-[#9b7b4d] mt-5 text-sm">
                            {{ service.link }}
                        </p>
                    </div>
                </RouterLink>
            </div>
        </div>
    </section>
</template>