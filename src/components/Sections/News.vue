<script setup>
import { ref, onMounted, onBeforeUnmount, computed } from 'vue';
import Headers from '../Common/Headers.vue';

const posts = ref([
    {
        link: '#',
        image: {
            src: 'https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/09/Blog-photos2-360x276@2x.jpg',
            alt: 'Blog Image 1',
            width: 262,
            height: 200,
        },
        date: 'January 10, 2014',
        comments: 0,
        title: 'He made the first step!',
        snippet: 'Working from home meant we could vary snack and coffee breaks, change our desks or…',
        author: 'Gary Jones',
        authorLink: '#',
        category: 'Legal Advice',
        categoryLink: '#',
    },
    {
        link: '#',
        image: {
            src: 'https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/09/Blog-photos3-360x276@2x.jpg',
            alt: 'Blog Image 2',
            width: 262,
            height: 200,
        },
        date: 'February 20, 2014',
        comments: 5,
        title: 'A New Perspective',
        snippet: 'Working from home meant we could vary snack and coffee breaks, change our desks or…',
        author: 'Jane Doe',
        authorLink: '#',
        category: 'Innovation',
        categoryLink: '#',
    },
    {
        link: '#',
        image: {
            src: 'https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/09/Blog-photos4-360x276@2x.jpg',
            alt: 'Blog Image 3',
            width: 262,
            height: 200,
        },
        date: 'March 15, 2014',
        comments: 3,
        title: 'The Next Step',
        snippet: 'New strategies for personal and professional growth.',
        author: 'Emily White',
        authorLink: '#',
        category: 'Strategy',
        categoryLink: '#',
    },
    {
        link: '#',
        image: {
            src: 'https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/09/Blog-photos5-360x276@2x.jpg',
            alt: 'Blog Image 4',
            width: 262,
            height: 200,
        },
        date: 'April 25, 2014',
        comments: 7,
        title: 'Breaking New Ground',
        snippet: 'Innovative approaches to modern challenges.',
        author: 'Michael Smith',
        authorLink: '#',
        category: 'Innovation',
        categoryLink: '#',
    },
]);

const currentIndex = ref(0);

const visiblePosts = computed(() => {
    const start = currentIndex.value;
    const end = Math.min(start + 2, posts.value.length);
    return posts.value.slice(start, end);
});

const showNext = () => {
    if (currentIndex.value + 2 < posts.value.length) {
        currentIndex.value += 2;
    }
};

const showPrevious = () => {
    if (currentIndex.value - 2 >= 0) {
        currentIndex.value -= 2;
    }
};

const beforeEnter = (el) => {
    el.style.opacity = 0;
};

const enter = (el, done) => {
    el.offsetHeight;
    el.style.transition = 'opacity 0.5s';
    el.style.opacity = 1;
    done();
};

const leave = (el, done) => {
    el.style.transition = 'opacity 0.5s';
    el.style.opacity = 0;
    done();
};



const currentBox = ref(0);

onMounted(() => {
    setInterval(() => {
        currentBox.value = (currentBox.value + 1) % 3;
    }, 5000); 
});






</script>

<template>
    <section class="text-[#4a4a4a]">
        <div class="containerr">
            <Headers text="LATEST NEWS & TESTIMONIALS"/>
        </div>

        <div class="lg:grid grid-cols-12 containerr">
            <div class="col-span-6">


                <div class="relative max-w-[1200px] mx-auto flex">
                    <transition name="fade" @before-enter="beforeEnter" @enter="enter" @leave="leave">
                        <div v-if="visiblePosts.length > 0" class="relative w-1/2 p-4 " :key="visiblePosts[0].link">
                            <RouterLink :to="visiblePosts[0].link">
                                <img :width="visiblePosts[0].image.width" :height="visiblePosts[0].image.height"
                                    :src="visiblePosts[0].image.src" :alt="visiblePosts[0].image.alt" />
                            </RouterLink>
                            <div class="mt-4">
                                <div class="flex items-center justify-between text-xs text-[#7c7f82] !mt-5">
                                    <p>{{ visiblePosts[0].date }}</p>
                                    <RouterLink :to="visiblePosts[0].link" target="_blank">
                                        <i class="ri-chat-2-line mr-2 hover:text-[#9b7b4d]"></i>
                                        <span class="text-[#9b7b4d]">{{ visiblePosts[0].comments }}</span>
                                    </RouterLink>
                                </div>
                                <RouterLink :to="visiblePosts[0].link">
                                    <h5 class="text-[#9b7b4d] text-xl mt-2">{{ visiblePosts[0].title }}</h5>
                                </RouterLink>
                                <span class="block border w-full mt-2"></span>
                                <p class="text-sm my-3">{{ visiblePosts[0].snippet }}</p>
                                <div class="mt-3.5 text-sm ">
                                    <RouterLink class="text-[#9b7b4d]" :to="visiblePosts[0].authorLink">{{
                                        visiblePosts[0].author }}
                                    </RouterLink>
                                    <p class="text-[#7c7f82]">
                                        Posted in:
                                        <RouterLink class="text-[#9b7b4d]" :to="visiblePosts[0].categoryLink">{{
                                            visiblePosts[0].category }}
                                        </RouterLink>
                                    </p>
                                </div>
                            </div>

                            <button @click="showPrevious"
                                class="absolute left-8 top-1/2 transform -translate-y-1/2 text-white p-1  opacity-80 hover:opacity-100 bg-[#4a4a4a]">
                                <i class="ri-arrow-left-line text-3xl"></i>
                            </button>
                        </div>
                    </transition>

                    <transition name="fade" @before-enter="beforeEnter" @enter="enter" @leave="leave">
                        <div v-if="visiblePosts.length > 1" class="relative w-1/2 p-4 " :key="visiblePosts[1].link">

                            <RouterLink :to="visiblePosts[1].link">
                                <img :width="visiblePosts[1].image.width" :height="visiblePosts[1].image.height"
                                    :src="visiblePosts[1].image.src" :alt="visiblePosts[1].image.alt" />
                            </RouterLink>
                            <div class="mt-4">
                                <div class="flex items-center justify-between text-xs text-[#7c7f82] !mt-5">
                                    <p>{{ visiblePosts[1].date }}</p>
                                    <RouterLink :to="visiblePosts[1].link" target="_blank">
                                        <i class="ri-chat-2-line mr-2 hover:text-[#9b7b4d]"></i>
                                        <span class="text-[#9b7b4d]">{{ visiblePosts[1].comments }}</span>
                                    </RouterLink>
                                </div>
                                <RouterLink :to="visiblePosts[1].link">
                                    <h5 class="text-[#9b7b4d] text-xl mt-2">{{ visiblePosts[1].title }}</h5>
                                </RouterLink>
                                <span class="block border w-full mt-2"></span>
                                <p class="text-sm my-3">{{ visiblePosts[1].snippet }}</p>
                                <div class="mt-3.5 text-sm ">
                                    <RouterLink class="text-[#9b7b4d]" :to="visiblePosts[1].authorLink">{{
                                        visiblePosts[1].author }}
                                    </RouterLink>
                                    <p class="text-[#7c7f82]">
                                        Posted in:
                                        <RouterLink class="text-[#9b7b4d]" :to="visiblePosts[1].categoryLink">{{
                                            visiblePosts[1].category }}
                                        </RouterLink>
                                    </p>
                                </div>
                            </div>

                            <button @click="showNext"
                                class="absolute right-8 top-1/2 transform -translate-y-1/2  text-white p-1 opacity-80 hover:opacity-100 bg-[#4a4a4a]">
                                <i class="ri-arrow-right-line text-3xl"></i>
                            </button>
                        </div>
                    </transition>
                </div>


            </div>
            <div class="col-span-6 ">
                <div class="p-4 flex items-start gap-8">
                    <div v-if="currentBox === 0" key="0" class="flex items-start gap-8">
                        <div>
                            <img width="120" height="120"
                                src="https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/03/people-3-250x250.jpg"
                                alt="">
                            <p class="text-sm mt-3">
                                Ashley Fletcher
                            </p>
                        </div>
                        <div class="flex flex-col justify-between max-w-[400px] gap-4">
                            <h2 class="text-3xl text-black">
                                Useless laws weaken the necessary laws.
                            </h2>
                            <div>
                                <i class="ri-star-fill text-[#CCA876] text-xl"></i>
                                <i class="ri-star-fill text-[#CCA876] text-xl"></i>
                                <i class="ri-star-fill text-[#CCA876] text-xl"></i>
                                <i class="ri-star-fill text-[#7C7F82] text-xl"></i>
                                <i class="ri-star-fill text-[#7C7F82] text-xl"></i>
                            </div>
                            <p class="text-sm">
                                Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium lectorum.
                            </p>
                            <p class="text-sm">
                                Mirum est notare quam littera gothica, quam nunc putamus parum claram, anteposuerit
                                litterarum formas humanitatis pe.
                            </p>
                            <img width="110" height="75"
                                src="https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/09/sign.gif" alt="">
                        </div>
                    </div>

                    <!--  -->

                    <div v-if="currentBox === 1" key="1" class="flex items-start gap-8">
                        <div>
                            <img width="120" height="120"
                                src="https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/03/people-1-250x250.jpg"
                                alt="">
                            <p class="text-sm mt-3">
                                John Doe
                            </p>
                        </div>
                        <div class="flex flex-col justify-between max-w-[400px] gap-4">
                            <h2 class="text-3xl text-black">
                                The best way to predict the future is to invent it.
                            </h2>
                            <div>
                                <i class="ri-star-fill text-[#CCA876] text-xl"></i>
                                <i class="ri-star-fill text-[#CCA876] text-xl"></i>
                                <i class="ri-star-fill text-[#CCA876] text-xl"></i>
                                <i class="ri-star-fill text-[#CCA876] text-xl"></i>
                                <i class="ri-star-fill text-[#7C7F82] text-xl"></i>
                            </div>
                            <p class="text-sm">
                                Nulla facilisi. Cras id dui lectus. Proin ut dolor auctor.
                            </p>
                            <p class="text-sm">
                                Nam malesuada pharetra felis. Fusce suscipit justo vitae auctor vehicula.
                            </p>
                            <img width="110" height="75"
                                src="https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/09/sign.gif" alt="">
                        </div>
                    </div>

                    <!--  -->

                    <div v-if="currentBox === 2" key="2" class="flex items-start gap-8">
                        <div>
                            <img width="120" height="120"
                                src="https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/03/people-2-250x250.jpg"
                                alt="">
                            <p class="text-sm mt-3">
                                Sarah Williams
                            </p>
                        </div>
                        <div class="flex flex-col justify-between max-w-[400px] gap-4">
                            <h2 class="text-3xl text-black">
                                Do not wait to strike till the iron is hot, but make it hot by striking.
                            </h2>
                            <div>
                                <i class="ri-star-fill text-[#CCA876] text-xl"></i>
                                <i class="ri-star-fill text-[#CCA876] text-xl"></i>
                                <i class="ri-star-fill text-[#CCA876] text-xl"></i>
                                <i class="ri-star-fill text-[#CCA876] text-xl"></i>
                                <i class="ri-star-fill text-[#CCA876] text-xl"></i>
                            </div>
                            <p class="text-sm">
                                Etiam fermentum nibh vel tellus euismod venenatis.
                            </p>
                            <p class="text-sm">
                                Nulla tincidunt dolor in facilisis congue.
                            </p>
                            <img width="110" height="75"
                                src="https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/09/sign.gif" alt="">
                        </div>
                    </div>

                </div>


                <div class="flex justify-center mt-6 space-x-3">
                    <span v-for="(box, index) in 3" :key="index" @click="currentBox = index"
                        :class="currentBox === index ? 'bg-[#CCA876]' : 'bg-gray-300'"
                        class="w-3 h-3 rounded-full cursor-pointer transition-colors duration-300"></span>
                </div>










            </div>
        </div>

    </section>
</template>

<style scoped>
.relative {
    position: relative;
}

.fade-enter-active,
.fade-leave-active {
    transition: opacity 0.5s;
}

.fade-enter,
.fade-leave-to

/* .fade-leave-active in <2.1.8 */
    {
    opacity: 0;
}

.absolute {
    position: absolute;
}





</style>