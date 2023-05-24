<template>
  <section class="w-full ">
    <header class="w-full border-b border-b-gray-200">
      <ul class="flex items-center text-sm font-semibold">
        <li class="p-4 text-blue-500">Active Jobs</li>
        <li class="p-4 text-gray-500 hover:bg-white">Inactive Jobs</li>
      </ul>
    </header>
    <main class="px-4 sm:pl-4 sm:pr-0">
      <div class="flex flex-col py-5 sm:items-end gap-0.5 text-gray-500 sm:gap-10  sm:flex-row sm:pr-4">
        <h2 class="text-2xl font-bold text-black">7 Active Jobs</h2>
        <p class="flex gap-2">
          Short by:
          <span class="flex items-center gap-0.5 text-sm font-bold text-black"
            >Creation Date
            <span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="w-4 h-4"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M8.25 15L12 18.75 15.75 15m-7.5-6L12 5.25 15.75 9"
                />
              </svg>
            </span>
          </span>
        </p>
        <p class="flex items-center gap-2">
          Status:
          <span class="flex items-center gap-0.5 text-sm font-bold text-black"
            >All Status
            <span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke-width="1.5"
                stroke="currentColor"
                class="w-4 h-4"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M8.25 15L12 18.75 15.75 15m-7.5-6L12 5.25 15.75 9"
                />
              </svg>
            </span>
          </span>
        </p>
      </div>
      <div class="flex flex-wrap gap-[18px] mb-3">
        <div v-for="(item,index) in data" :key="index" class="w-full p-2 bg-white border-t-4 rounded-md sm:w-56 lg:w-[16rem]" :class="{'border-t-red-500' : item.red} ,{'border-t-green-500':!item.red}">
          <h1 class="text-2xl font-bold text-gray-500">{{item.title}}</h1>
          <p class="mb-3 font-bold">{{ item.role }}</p>
          <span class="text-sm text-gray-500">Candidates:</span>
          <div class="flex items-center w-full p-2 mt-1 border-2 border-gray-200 rounded-md bg-slate-300">
            <div class="flex flex-col w-1/2 px-1 border-l-4 border-l-green-500">
              <span  class="text-sm font-bold text-gray-600">TOTAL</span>
              <span class="text-lg font-bold">{{ item.total }}</span>
            </div>
            <div class="flex flex-col w-1/2 px-1 border-l-4 border-l-green-500">
              <span class="text-sm font-bold text-gray-600">NEW</span>
              <span class="text-lg font-bold">{{ item.new }}</span>
            </div>
          </div>
          <h2 class="py-1 text-lg font-bold text-center text-gray-700 border-b border-b-gray-300">Purwokerto . Freelancer</h2>
          <div class="flex items-center justify-between mt-1.5 text-gray-700">
            <span class="flex itemc-center"><ClipboardDocumentListIcon class="inline w-6 h-6"/> Draft</span>
            <span>See Details</span>
          </div>
        </div>
      </div>
    </main>
  </section>
</template>

<script setup>
import {ClipboardDocumentListIcon} from '@heroicons/vue/24/outline'
const data=[
    {
      title:'Design',
      role:'Senior Product Designer',
      total:36,
      red:true,
      new:5,
    },
    {
      title:'Design',
      role:'UI/UX Designer',
      total:23,
      red:false,
      new:2,
    },
    {
      title:'Developer',
      role:'Senior Developer',
      total:42,
      red:true,
      new:2,
    },
    {
      title:'Design',
      role:'Head of UX',
      total:16,
      red:false,
      new:4,
    },
    {
      title:'Marketing',
      role:'Copywriter',
      total:27, 
      red:true,
      new:9,
    },
    {
      title:'Design',
      role:'Senior Product Designer',
      total:36,
      red:false,
      new:5,
    },
]
</script>


