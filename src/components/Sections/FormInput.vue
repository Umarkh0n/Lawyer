<script setup>
import Buttons from '../Common/Buttons.vue';
import Headers from '../Common/Headers.vue';


</script>

<template>
    <section class=" ">
        <div class="containerr">
            <div class="mt-[120px] flex items-center text-[#4a4f55]">
                <span class="block border w-full"></span>
                <h2 class=" mb-3 text-2xl font-sans text-center uppercase text-[#4a4f55] lg:min-w-[680px]">
                    Want to be an intern with us and you are a student?
                </h2>
                <span class="block border w-full"></span>
            </div>
            <p class="text-sm text-center my-[30px] max-w-[650px] mx-auto">
                Claritas est etiam processus dynamicus, qui sequitur mutationem consuetudium lectorum. Claritas
                est etiam processus dynamicus, qui sequitur mutationem…
            </p>
            <div class="flex justify-center">
                <Buttons text="Apply now" variant="unusual" :showIcon="true" icon-class="ri-send-plane-fill text-2xl !text-[#7C7F82]" />
            </div>
        </div>

        <div class="baground bg-cover bg-no-repeat mt-[80px]">
            <div class="containerr">
                <Headers class="!pt-[1px]" text="REQUEST A FREE CONSULTATION" />
                <p class="mx-auto text-center text-lg text-[#7c7f82;] pb-[60px]">
                    Fill out the form below to recieve a free and confidential intial consultation.
                </p>

                <form class="">


                    <div class="lg:flex items-center justify-between gap-[30px]">

                        <input class="mt-6 lg:mt-0 shadow px-4 py-3 w-full border-gray-300 focus:ring-1 focus:ring-[#cca876] focus:border-[#cca876] focus:outline-none placeholder-gray-500 transition duration-200 ease-in-out" type="text" placeholder="Name">


                        <input class="mt-6 lg:mt-0 shadow px-4  py-3 w-full border-gray-300 focus:ring-1 focus:ring-[#cca876] focus:border-[#cca876] focus:outline-none placeholder-gray-500 transition duration-200 ease-in-out" type="text" placeholder="Phone">

                        <select class="mt-6 lg:mt-0 shadow w-full px-4 text-[#7c7f82;] py-3.5 border-gray-300 focus:ring-1 focus:ring-[#cca876] focus:border-[#cca876] focus:outline-none placeholder-gray-500 transition duration-200 ease-in-out" name="" id="">
                            <option value="Family law">Family law</option>
                            <option value="Business Law">Business Law</option>
                            <option value="Civil Litigation">Civil Litigation</option>
                            <option value="Other">Other</option>
                        </select>
                    </div>
                    <div>
                        <textarea
                            class="shadow w-full mt-6 p-4 border border-gray-300 focus:ring-1 focus:ring-[#cca876] focus:border-[#cca876] focus:outline-none placeholder-gray-500 transition duration-200 ease-in-out"
                            cols="40" rows="5" maxlength="400" placeholder="Case Description..."></textarea>
                    </div>
                    <div class="pb-16">
                        <Buttons text="SEND REQUEST →" variant="primary" class="mx-auto mt-8 "/>
                    </div>
                </form>
            </div>
        </div>

    </section>
</template>

<style scoped>
.baground {
    background-image: url("https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/09/bg_1.jpg");
}
</style>