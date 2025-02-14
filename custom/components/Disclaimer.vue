<template>
    <div class="alert alert-error text-white hidden">
        <Fa :icon="faCircleInfo" />
        <p class="text-sm">
            Dies ist ein Demo Store von PocketStore.io, die Bestellungen werden nicht ausgeführt.
        </p>
        <Fa :icon="faCircleInfo" />
    </div>
</template>

<script setup lang="ts">
import { faCircleInfo } from '@fortawesome/free-solid-svg-icons'
</script>