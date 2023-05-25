<template>
  <header class="flex gap-5 px-4 py-3 font-bold border-b border-gray-200">
    <span class="text-blue-600">RECRUITMENT INBOX</span>
    <span class="text-gray-600">WORK INBOX</span>
  </header>
  <main class="grid grid-cols-12 overflow-y-hidden">
    <section class="col-span-12 p-4 border-r border-gray-200 lg:col-span-3">
      <form class="flex items-center gap-2">
        <label for="simple-search" class="sr-only">Search</label>
        <div class="relative w-full">
          <div
            class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none"
          >
            <svg
              class="w-5 h-5 text-gray-500"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
              ></path>
            </svg>
          </div>
          <input
            type="text"
            id="simple-search"
            v-model="searchText"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full pl-10 p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
            placeholder="Search"
            required
          />
        </div>
        <button
          type="submit"
          class="p-2 ml-2 text-sm font-medium text-gray-500 bg-gray-100 border border-gray-200 rounded-lg"
        >
          <FunnelIcon class="w-6 h-6 text-gray-500" />
          <span class="sr-only">Search</span>
        </button>
      </form>
      <div class="flex flex-col lg:h-[32rem] py-2 gap-2 mt-4 lg:overflow-y-auto no-scrollbar">
        <div
          v-for="(item, index) in data"
          :key="index"
          class="flex items-center gap-2 px-5 py-5 text-gray-500 bg-white rounded-md sm:px-1 h-28"
          :class="{'!bg-slate-300':index===2}"
        >
          <img
            :src="item.image"
            class="object-cover w-12 h-12 rounded-full"
            alt="dp"
          />
          <div class="w-full">
            <div class="flex items-center justify-between">
              <h4 class="font-bold text-black">{{ item.name }}</h4>
              <span class="text-sm">{{ item.time }} Days ago</span>
            </div>
            <div class="mt-1 text-sm">Job: {{ item.job }}</div>
            <div class="text-sm">{{ item.team }}</div>
          </div>
        </div>
      </div>
    </section>
    <section class="col-span-12 border-r border-gray-200 lg:col-span-6">
      <div class="flex items-center justify-between p-4 border-b border-b-gray-200">
        <div>
          <h4 class="text-sm font-bold">My Application for Senior Developer</h4>
          <span>Job: Front-End Developer</span>
        </div>
        <div
          class="flex items-center h-10 px-1 font-bold bg-gray-400 rounded-lg md:h-auto"
        >
          <span class="px-3 py-1 md:py-1.5 bg-white rounded-md">Chat</span>
          <span class="px-3 py-1 md:py-1.5 text-gray-800">Email</span>
        </div>
      </div>
      <div class="w-full lg:h-[29rem]  lg:overflow-y-auto">

        <div class="relative mt-8 border-t border-t-gray-200">
          <span class="absolute top-0 px-3 py-1 text-xs font-semibold text-white -translate-x-1/2 -translate-y-1/2 bg-black rounded-full left-1/2">Fri, 2 Jul</span>
          <div class="flex flex-col w-full gap-4 px-4 py-8">
            <p class="w-[95%] p-2 bg-white rounded-lg md:w-3/5">Hello, Here is the file you requared before. Please, Checkout this assesment, and let me know if you need something else.</p>
          <p class="flex items-center justify-between w-[95%] p-2 bg-white rounded-lg md:w-3/5">
            <div class="flex items-center gap-2">
              <DocumentTextIcon class="w-6 h-6 "/>
              <p>
                <strong class="block">CV New.doc</strong>
                <span class="block text-gray-500">1.2 Mb</span>
              </p>
            </div>
            <ArrowDownTrayIcon class="w-6 h-6"/>
          </p>
        </div>
      </div>
      <div class="relative border-t border-t-gray-200">
        <span class="absolute top-0 px-3 py-1 text-xs font-semibold text-white -translate-x-1/2 -translate-y-1/2 bg-black rounded-full left-1/2">Today</span>
        <div class="relative flex items-end w-full h-64 gap-4 px-4 py-8">
            <p class="absolute w-[85%] p-2 bg-green-300 rounded-lg md:w-3/5 top-8 right-4">Hello Cody, Thank you, I will check it out and let you know if we need somthing else. Thanks.</p>
            <p class="w-[90%] p-2 bg-white rounded-lg md:w-3/5">Hello Cody, Thank you, I will check it out and let you know if we need somthing else. Thanks.</p>
        </div>
      </div>
    </div>
      <div class="flex items-center w-full gap-3 px-5 py-2 bg-gray-50">
        <PhotoIcon class="text-gray-500 w-7 h-7" />
        <FaceSmileIcon  class="text-gray-500 w-7 h-7" />
        <input type="text" id="first_name" class="bg-gray-50 border flex-grow border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5" placeholder="John" required>
        <PaperAirplaneIcon class="text-blue-600 w-7 h-7" />
      </div>
    </section>
    <section class="col-span-12 lg:h-[37rem] lg:col-span-3 lg:overflow-y-auto new-scrollbar">
      <div class="flex flex-col items-center p-4 border-b border-b-gray-200">
        <img :src="data[2].image" alt="dp" class="w-16 h-16 rounded-full">
        <h3 class="mt-2 font-bold ">{{ data[2].name }}</h3>
        <p class="text-sm text-gray-500">View Profile</p>
      </div>
      <div class="p-2 border-b md:p-4 border-b-gray-200">
        <p class="text-xs font-bold">Applied For:</p>
        <h4 class="font-bold">Job: Senior UIX Designer</h4>
        <span class="text-sm text-gray-500">Design Team</span>
        <div class="flex gap-0.5 item-center">
          <StarIcon  class="w-[1.15rem] h-[1.15rem] text-yellow-400"/>
          <StarIcon  class="w-[1.15rem] h-[1.15rem] text-yellow-400"/>
          <StarIcon  class="w-[1.15rem] h-[1.15rem] text-yellow-400"/>
          <StarIcon  class="w-[1.15rem] h-[1.15rem] text-yellow-400"/>
          <StarIcon  class="w-[1.15rem] h-[1.15rem] text-gray-300"/>
        </div>
      </div>
      <div class="p-2 border-b md:p-4 border-b-gray-200">
        <span class="flex items-center gap-1 mb-2"><EnvelopeIcon class="w-6 h-6" /> codyfish@gmail.com</span>
        <span class="flex items-center gap-1"><PhoneIcon class="w-6 h-6"/>+916482354685 </span>
      </div>
      <div class="p-2 border-b md:p-4 border-b-gray-200">
        <span class="flex items-center gap-1 font-bold text-blue-600"><PlusCircleIcon  class="w-6 h-6 text-blue-600"/>Add Owner</span>
      </div>
      <div class="p-2 mb-3 md:p-4">
        <span class="text-sm font-bold ">Schedule:</span>
        <div class="flex flex-col gap-2 px-2 py-3 mt-2 border border-l-4 border-gray-200 rounded-md border-l-green-400" >
          <p class="font-bold text-gray-700">Allignment for onboarding welcoming new menber on Product Teams</p>
          <span class="w-32 py-0.5 text-xs font-semibold text-center text-blue-900 bg-blue-100 border border-blue-500 rounded-md">Waiting Approval</span>
          <span class="text-sm ">9 Mar, 2021 7:00-7:45pm</span>
          <span class="text-xs font-bold">View Summery</span>
        </div>
      </div>
    </section>
  </main>
</template>

<script setup>
import { FunnelIcon } from "@heroicons/vue/24/outline";
import { StarIcon } from "@heroicons/vue/24/solid";
import { DocumentTextIcon } from "@heroicons/vue/24/outline";
import { ArrowDownTrayIcon } from "@heroicons/vue/24/outline";
import { PhotoIcon } from "@heroicons/vue/24/outline";
import { FaceSmileIcon } from "@heroicons/vue/24/outline";
import { PaperAirplaneIcon } from "@heroicons/vue/24/outline";
import { EnvelopeIcon } from "@heroicons/vue/24/outline";
import { PhoneIcon } from "@heroicons/vue/24/outline";
import { PlusCircleIcon } from "@heroicons/vue/24/outline";
const searchText = ref("");

const data = [
  {
    name: "Brooklyn Simmons",
    image: "https://flowbite.com/docs/images/people/profile-picture-1.jpg",
    job: "Senior UIX Designer",
    team: "Design Team",
    time: 1,
  },
  {
    name: "Ronaldo Karvia",
    image: "https://flowbite.com/docs/images/people/profile-picture-2.jpg",
    job: "UI/UX Designer",
    team: "Design Team",
    time: 1,
  },
  {
    name: "Coddy Fisher",
    image: "https://flowbite.com/docs/images/people/profile-picture-3.jpg",
    job: "Front-End Developer",
    team: "Developer Team",
    time: 1,
  },
  {
    name: "Airlen McKoi",
    image: "https://flowbite.com/docs/images/people/profile-picture-4.jpg",
    job: "Web Designer",
    team: "Design Team",
    time: 1,
  },
  {
    name: "Darlane Robert",
    image: "https://flowbite.com/docs/images/people/profile-picture-5.jpg",
    job: "Web Designer",
    team: "Design Team",
    time: 1,
  },
  {
    name: "Robarto Carlose",
    image: "https://flowbite.com/docs/images/people/profile-picture-2.jpg",
    job: "Web Developer",
    team: "Developer Team",
    time: 1,
  },
];
</script>

<style>
.no-scrollbar::-webkit-scrollbar{
  display: none;
  scrollbar-width: none;
} 
.new-scrollbar::-webkit-scrollbar-thumb{
  @apply bg-gray-300
}
</style>