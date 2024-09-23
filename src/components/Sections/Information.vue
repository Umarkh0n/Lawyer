<script setup>
import Headers from '../Common/Headers.vue';

const people = [
  {
    name: "Ashley Fletcher",
    role: "Lawyer & CEO",
    email: "support@vamtam.com",
    phone: "800-700-6200",
    image: "https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/03/people-1.jpg",
    profileLink: "#",
    socials: [
      { iconClass: "ri-google-fill", link: "/" },
      { iconClass: "ri-instagram-fill", link: "/" },
      { iconClass: "ri-facebook-fill", link: "/" },
      { iconClass: "ri-twitter-fill", link: "/" }
    ]
  },
  {
    name: "John Doe",
    role: "CTO",
    email: "john@vamtam.com",
    phone: "800-123-4567",
    image: "https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/03/people-2.jpg",
    profileLink: "#",
    socials: [
      { iconClass: "ri-google-fill", link: "/" },
      { iconClass: "ri-instagram-fill", link: "/" },
      { iconClass: "ri-facebook-fill", link: "/" },
      { iconClass: "ri-twitter-fill", link: "/" }
    ]
  },
  {
    name: "Emily Clark",
    role: "HR Manager",
    email: "emily@vamtam.com",
    phone: "800-987-6543",
    image: "https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/03/people-3.jpg",
    profileLink: "#",
    socials: [
      { iconClass: "ri-google-fill", link: "/" },
      { iconClass: "ri-instagram-fill", link: "/" },
      { iconClass: "ri-facebook-fill", link: "/" },
      { iconClass: "ri-twitter-fill", link: "/" }
    ]
  },
  {
    name: "Michael Brown",
    role: "CFO",
    email: "michael@vamtam.com",
    phone: "800-555-1212",
    image: "https://lawyers-attorneys.vamtam.com/wp-content/uploads/2014/03/people-4.jpg",
    profileLink: "#",
    socials: [
      { iconClass: "ri-google-fill", link: "/" },
      { iconClass: "ri-instagram-fill", link: "/" },
      { iconClass: "ri-facebook-fill", link: "/" },
      { iconClass: "ri-twitter-fill", link: "/" }
    ]
  }
];

</script>

<template>
  <section class="containerr">
    <div>
      <Headers text="MEET OUR ATTORNEYS" />
    </div>
    <div class="lg:flex items-center  lg:justify-between gap-[30px]">
      <div v-for="(person, index) in people" :key="index" class="profile text-center lg:text-start mt-32 lg:mt-0">
        <RouterLink :to="person.profileLink">
          <img :src="person.image" :alt="person.name" class="mx-auto">
        </RouterLink>
        <div class="p-1">
          <h3 class="text-xl font-serif mt-1">
            {{ person.name }}
          </h3>
          <p class="text-sm text-[#7c7f82]">
            {{ person.role }}
          </p>
          <span class="block border w-full my-3"></span>
          <div>
            <RouterLink class="block text-[#9b7b4d] text-sm" target="_blank" :href="'mailto:' + person.email">
              {{ person.email }}
            </RouterLink>
            <RouterLink class="text-sm" :href="'tel:' + person.phone">
              Tel: {{ person.phone }}
            </RouterLink>
          </div>
          <div class="flex items-center justify-center lg:justify-start gap-3 text-xl mt-3 mb-2">
            <RouterLink v-for="(icon, i) in person.socials" :key="i" :to="icon.link" target="_blank" class="group">
              <i :class="icon.iconClass + ' text-[#d8d8d8] group-hover:text-[#cca876;] transition-all'"></i>
            </RouterLink>
          </div>
          <span class="block border w-full"></span>
        </div>
      </div>
    </div>


  </section>
</template>