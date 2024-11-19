<template>
    <div class="alert alert-error text-white">
        <Fa :icon="faCircleInfo" />
        <p class="text-sm">
            This is a Demo Storefront from PocketStore.io and for the moment no real Store
        </p>
        <Fa :icon="faCircleInfo" />
    </div>
</template>

<script setup lang="ts">
import { faCircleInfo } from '@fortawesome/free-solid-svg-icons'
</script>