<template>
    <div v-if="route.path == '/de'" class="grid grid-cols-6 gap-3">
        <div class="col-span-6 md:col-span-1">
            <div class="w-full bg-[#1e1f26] h-24 flex items-center justify-center rounded-lg">
                <Fa :icon="faBowlingBall" color="white" size="2x"></Fa>
                <span class="text-white font-bold ml-3">Bowling</span>
            </div>
        </div>
        <div class="col-span-6 md:col-span-1">
            <div class="w-full bg-[#1e1f26] h-24 flex items-center justify-center rounded-lg">
                <Fa :icon="faGun" color="white" size="2x"></Fa>
                <span class="text-white font-bold ml-3">Paintball</span>
            </div>
        </div>
        <div class="col-span-6 md:col-span-1">
            <div class="w-full bg-[#1e1f26] h-24 flex items-center justify-center rounded-lg">
                <Fa :icon="faComputer" color="white" size="2x"></Fa>
                <span class="text-white font-bold ml-3">Geek</span>
            </div>
        </div>
        <div class="col-span-6 md:col-span-1">
            <div class="w-full bg-[#1e1f26] h-24 flex items-center justify-center rounded-lg">
                <Fa :icon="faGun" color="white" size="2x"></Fa>
                <span class="text-white font-bold ml-3">Paintball</span>
            </div>
        </div>
        <div class="col-span-6 md:col-span-1">
            <div class="w-full bg-[#1e1f26] h-24 flex items-center justify-center rounded-lg">
                <Fa :icon="faFilm" color="white" size="2x"></Fa>
                <span class="text-white font-bold ml-3">Filme</span>
            </div>
        </div>
        <div class="col-span-6 md:col-span-1">
            <div class="w-full bg-[#1e1f26] h-24 flex items-center justify-center rounded-lg">
                <Fa :icon="faDartLang" color="white" size="2x"></Fa>
                <span class="text-white font-bold ml-3">Dart</span>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { faBowlingBall, faGun, faFilm, faComputer } from '@fortawesome/free-solid-svg-icons'
import { faDartLang } from '@fortawesome/free-brands-svg-icons'
import {useRoute} from 'vue-router'

const route = useRoute();
</script>