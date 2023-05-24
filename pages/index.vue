<template>
  <section class="w-full p-2 mb-5 sm:px-6">
    <header class="py-2">
      <div
        class="flex flex-col justify-between gap-2 sm:items-center sm:flex-row"
      >
        <div>
          <h2 class=" font-bold text-xl">Senior Product Designer</h2>
          <span class="text-gray-500 text-sm">Purwokerto . Full Time</span>
        </div>
        <div class="sm:text-right">
          <button
            type="button"
            class="focus:outline-none text-white bg-green-700 hover:bg-green-800 focus:ring-4 focus:ring-green-300 font-medium rounded-lg  text-sm px-5 py-2.5 mr-2 mb-2"
          >
            Share & Promote
          </button>
          <button
            type="button"
            class="focus:outline-none text-white bg-green-700 hover:bg-green-800 focus:ring-4 focus:ring-green-300 font-medium rounded-lg  text-sm px-5 py-2.5 mr-2 mb-2"
          >
            Published
          </button>
        </div>
      </div>
      <nav class="mt-5 leading-4">
        <ul
          class="flex flex-wrap gap-3  font-bold text-gray-500 sm:gap-5 lg:gap-10"
        >
          <li class="text-black">Candidate</li>
          <li>Job Details</li>
          <li>Time Line</li>
          <li>Hiring Team</li>
          <li>Settings</li>
        </ul>
      </nav>
      <hr class="mt-2" />
    </header>
    <div
      class="flex flex-col justify-between gap-2 mt-5 sm:items-center sm:flex-row"
    >
      <div class="font-bold">
        Total Candidate:
        <span class="p-0.5 mx-2 text-white bg-green-700 rounded-sm">22</span>
      </div>
      <div
        class="flex items-center gap-2 p-1 font-bold bg-gray-400 rounded-md w-60"
      >
        <span class="px-2 py-1 bg-white rounded-md">Pipeline View</span>
        <span class="px-2 py-1 text-gray-800">Table View</span>
      </div>
    </div>
    <main class="grid w-full grid-cols-12 gap-10 mt-5">
      <div
        id="New Applied"
        class="col-span-12 mr-1 sm:mr-0 sm:col-span-6 xl:col-span-3"
      >
        <div
          class="flex justify-between p-3 font-bold bg-white border-t-4 rounded-md border-t-green-500"
        >
          <span>New Applied</span> <span>10</span>
        </div>
        <div class="flex flex-col items-center gap-3 mt-5">
          <Candidate
            v-for="(item, index) in data.new"
            :key="index"
            v-bind="item"
          />
        </div>
      </div>
      <div
        id="Screening"
        class="col-span-12 mr-1 sm:mr-0 sm:col-span-6 xl:col-span-3"
      >
        <div
          class="flex justify-between p-3 font-bold bg-white border-t-4 rounded-md border-t-yellow-500"
        >
          <span>Screening</span> <span>3</span>
        </div>
        <div class="flex flex-col items-center gap-3 mt-5">
          <Candidate
            v-for="(item, index) in data.screening"
            :key="index"
            v-bind="item"
          />
        </div>
      </div>
      <div
        id="Design Challenge"
        class="col-span-12 mr-1 sm:mr-0 sm:col-span-6 xl:col-span-3"
      >
        <div
          class="flex justify-between p-3 font-bold bg-white border-t-4 rounded-md border-t-red-500"
        >
          <span>Design Challenge</span> <span>12</span>
        </div>
        <div class="flex flex-col items-center gap-3 mt-5">
          <Candidate
            v-for="(item, index) in data.new"
            :key="index"
            v-bind="item"
          />
        </div>
      </div>
      <div
        id="Interview"
        class="col-span-12 mr-1 sm:mr-0 sm:col-span-6 xl:col-span-3"
      >
        <div
          class="flex justify-between p-3 font-bold bg-white border-t-4 rounded-md border-t-violet-500"
        >
          <span>Interview</span> <span>2</span>
        </div>
        <div class="flex flex-col items-center gap-3 mt-5">
          <Candidate
            v-for="(item, index) in data.interview"
            :key="index"
            v-bind="item"
          />
        </div>
      </div>
    </main>
  </section>
</template>

<script setup>
const data = {
  new: [
    {
      name: "Esther Gongela",
      image: "https://flowbite.com/docs/images/people/profile-picture-5.jpg",
      rating: 4,
      time: 1,
    },
    {
      name: "Lubrica Fannandes",
      image: "https://flowbite.com/docs/images/people/profile-picture-1.jpg",
      rating: 5,
      time: 2,
    },
    {
      name: "Ariyana Grozza",
      image: "https://flowbite.com/docs/images/people/profile-picture-2.jpg",
      rating: 3,
      time: 2,
    },
    {
      name: "John Morchien",
      image: "https://flowbite.com/docs/images/people/profile-picture-3.jpg",
      rating: 5,
      time: 2,
    },
  ],
  screening: [
    {
      name: "Roushan Ambani",
      image: "https://flowbite.com/docs/images/people/profile-picture-3.jpg",
      rating: 4,
      time: 1,
    },
    {
      name: "Rubayet Jaman",
      image: "https://flowbite.com/docs/images/people/profile-picture-4.jpg",
      rating: 5,
      time: 2,
    },
    {
      name: "Ray Mistirayo",
      image: "https://flowbite.com/docs/images/people/profile-picture-1.jpg",
      rating: 3,
      time: 2,
    },
  ],
  interview: [
    {
      name: "Shown Micalle",
      image: "https://flowbite.com/docs/images/people/profile-picture-1.jpg",
      rating: 3,
      time: 1,
    },
    {
      name: "Stone Chold",
      image: "https://flowbite.com/docs/images/people/profile-picture-3.jpg",
      rating: 5,
      time: 2,
    },
  ],
};
</script>
