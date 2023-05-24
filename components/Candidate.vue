<template>
    <div class="w-full bg-white rounded-md">
        <div class="flex items-center gap-2 p-2"><img :src="image" alt="person image" class="object-cover w-10 h-10 rounded-full" /> <span class="font-bold">{{name}}</span> </div>
        <hr class="mx-2">
        <div class="flex items-center justify-between p-2">
            <div id="star" class="flex">
                <div v-for="n in rating" :key="n">
                    <StarIcon  class="w-[1.15rem] h-[1.15rem] text-yellow-400"/>
                </div>
                <StarIcon v-for="n in (5-rating)" :key="n" class="w-[1.15rem] h-[1.15rem] text-gray-300"/>
            </div>
            <span>{{ time }} days ago</span>
        </div>
    </div>
</template>

<script setup>
import { StarIcon } from '@heroicons/vue/24/solid'


const {name,rating,image,time}=defineProps(['name','image','rating','time'])
</script>

