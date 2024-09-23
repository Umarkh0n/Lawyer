<script setup>
import { ref } from 'vue';
import Headers from '../Common/Headers.vue';

const activeIndex = ref(1);
const blocks = ref([
  { id: 1, title: 'How we can help you?', content: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip..' },
  { id: 2, title: 'How we can help you?', content: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip..' },
  { id: 3, title: 'How we can help you?', content: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip..' },
  { id: 4, title: 'How we can help you?', content: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip..' }
]);

const toggleVisibility = (id) => {
  activeIndex.value = id;
};
</script>




<template>
    <section>
        <div class="containerr text-center">
            <Headers text=" WHO WE ARE"/> 
            <div class=" font-serif">
                <h3 class="text-3xl">
                    “Every mountain top is within reach if you just keep climbing.”
                </h3>
                <p class="my-3 max-w-[670px] mx-auto text-sm">
                    Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorperadipiscing elit, sed diam
                    nonummy nibh suscipit lobortis nisl ut aliquip ex ea commodo consequat.
                </p>
                <RouterLink to="/" class="my-3 text-[#9b7b4d] hover:text-[#8e6020] transition text-sm uppercase">
                    — RICHARD JAMES MOLLOY

                </RouterLink>
            </div>
        </div>
        <div class="containerr block lg:grid grid-cols-12 !mt-[50px]">
            <div class="col-span-6 block lg:grid grid-cols-12">
                <div class="col-span-4">
                    <h3 class="uppercase my-2.5 px-[15px]">OUR HISTORY:</h3>
                    <div>
                        
                        <div class=" bg-[#4a4a4a]">
                            <img class="min-h-[420px] mx-auto lg:w-full max-h-[420px] "
                            src="https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/09/photo-1.png" alt="">
                            <ul class="px-[20px] py-[30px]">
                                <li class="mt-1 ml-2">
                                    <RouterLink to="/" active-class="active"
                                        class="text-[#cca876] hover:text-[#8e6020] text-sm uppercase">
                                        FAQ →
                                    </RouterLink>
                                </li>
                                <li class="mt-1 ml-2">
                                    <RouterLink to="/" active-class="active"
                                        class="text-[#cca876] hover:text-[#8e6020] text-sm uppercase">
                                        CLIENTS →
                                    </RouterLink>
                                </li>
                                <li class="mt-1 ml-2">
                                    <RouterLink to="/" active-class="active"
                                        class="text-[#cca876] hover:text-[#8e6020] text-sm uppercase">
                                        CONTACT US →
                                    </RouterLink>
                                </li>
                                <li class="mt-1 ml-2">
                                    <RouterLink to="/" active-class="active"
                                        class="text-[#cca876] hover:text-[#8e6020] text-sm uppercase">
                                        TESTIMONIALS →
                                    </RouterLink>
                                </li>
                                <li class="mt-1 ml-2">
                                    <RouterLink to="/" active-class="active"
                                        class="text-[#cca876] hover:text-[#8e6020] text-sm uppercase">
                                        ATTORNEYS →
                                    </RouterLink>
                                </li>
                            </ul>
                        </div>
                        <img class="px-[15px] py-[30px]"
                            src="https://lawyers-attorneys.vamtam.com/wp-content/uploads/2013/03/sign2.jpg" alt="">
                    </div>
                </div>
                <div class="col-span-8 px-[15px]">

                    <h3 class="text-xl mt-[40px] font-semibold font-sans">
                        <span class="text-[#cca876]">– 1987</span>, Opening
                    </h3>
                    <p class="px-5 my-3  text-sm">
                        Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod
                        tincidunt ut laoreet dolore magna aliquam erat volutpat.
                    </p>
                    <p class="px-5   text-sm">
                        Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorperadipiscing elit, sed diam
                        nonummy nibh suscipit lobortis nisl ut aliquip ex ea commodo consequat.
                    </p>
                    <!--  -->
                    <h3 class="text-xl mt-[40px] font-semibold font-sans">
                        <span class="text-[#cca876]">– 1996</span>, 30 fresh new people
                    </h3>
                    <p class="px-5 my-3  text-sm">
                        Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod
                        tincidunt ut laoreet dolore magna aliquam erat volutpat.
                    </p>
                    <p class="px-5   text-sm">
                        Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut
                        aliquip ex ea commodo consequat.
                    </p>
                    <!--  -->
                    <h3 class="text-xl mt-[40px] font-semibold font-sans">
                        <span class="text-[#cca876]">– 2014</span>, We’re in Tokyo!
                    </h3>
                    <p class="px-5 my-3  text-sm">
                        Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut
                        aliquip ex ea commodo consequat.
                        Accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore
                        te feugait nulla facilisi.
                    </p>
                    <p class="px-5  text-sm">
                        Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet…
                    </p>
                    <div class="mt-5">
                        <RouterLink to="/about"
                            class="px-5 !mt-[40px] text-[#cca876] hover:text-[#8e6020] text-sm uppercase">
                            READ FULL STORY →
                        </RouterLink>
                    </div>
                </div>
            </div>
            <div class="col-span-6">
                <h3 class="uppercase my-2.5 px-[15px]">HOW WE CAN HELP YOU:</h3>
                <div class="help_you w-full h-[360px]">
                    <div class=" h-full py-[30px] px-[20px] max-w-[300px] you text-white">
                        <div class="mt-20">
                            <RouterLink to="/" class="text-base">
                                Serious car crash <span class="text-[#cca876] ">→</span>
                            </RouterLink>
                        </div>
                        <div class="mt-2">
                            <RouterLink to="/" class="text-base">
                                Brain injury <span class="text-[#cca876] ">→</span>
                            </RouterLink>
                        </div>
                        <div class="mt-2">
                            <RouterLink to="/" class="text-base">
                                Truck accidents <span class="text-[#cca876] ">→</span>
                            </RouterLink>
                        </div>
                        <div class="mt-2">
                            <RouterLink to="/" class="text-base">
                                Semi-truck collision <span class="text-[#cca876] ">→</span>
                            </RouterLink>
                        </div>
                        <div class="mt-2">
                            <RouterLink to="/" class="text-base">
                                Motorcycle accidents <span class="text-[#cca876] ">→</span>
                            </RouterLink>
                        </div>
                        <div class="mt-2">
                            <RouterLink to="/" class="text-base">
                                Wrongful Death <span class="text-[#cca876] ">→</span>
                            </RouterLink>
                        </div>
                        <div class="mt-2">
                            <RouterLink to="/" class="text-base">
                                Sexual abuse <span class="text-[#cca876] ">→</span>
                            </RouterLink>
                        </div>
                    </div>
                </div>
                <!--  -->


                <div class="">
                    <div v-for="block in blocks" :key="block.id" class="py-5 px-8 border-b border-x">
                        <div @click="toggleVisibility(block.id)"
                            class="flex items-center justify-between cursor-pointer">
                            <h1 class="text-lg">{{ block.title }}</h1>
                            <button class="ml-4 px-4 py-2 rounded transition-all text-lg">
                                {{ activeIndex === block.id ? '-' : '+' }}
                            </button>
                        </div>
                        <div>
                            <Transition name="slide">
                                <p v-show="activeIndex === block.id" class="mt-6 text-sm">
                                    {{ block.content }}
                                </p>
                            </Transition>
                        </div>
                    </div>
                </div>







            </div>
        </div>

    </section>
</template>

<style scoped>
.active {
    color: #cca876;
}

.help_you {

    background: url('https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/09/bg_4.jpg') no-repeat center top;
    background-size: cover;
    background-attachment: scroll;
    padding-top: 0px;
    padding-bottom: 0px
}

.you {

    background: url('https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/09/bg-trans.png') repeat;
    background-size: auto;
    padding-top: 30px;
    padding-bottom: 30px;

}

.slide-enter-active,
.slide-leave-active {
    transition: all 0.5s ease;
}

.slide-enter,
.slide-leave-to {
    transform: translateY(20px);
    /* Pastdan tepaga ochilishi */
    opacity: 0;
}
</style>