<template>
    <nav class="hidden md:block">
        <ul class="flex space-x-3">
            <li>
                <a href="">
                    <Fa :icon="faBowlingBall"></Fa>
                    <span></span>
                </a>
            </li>
        </ul>
    </nav>
</template>

<script lang="ts" setup>
import { faBowlingBall } from '@fortawesome/free-solid-svg-icons'
</script>