<template>
    <section style="background-image:url('/2024-beekeeper.jpeg')" class="min-h-screen bg-cover">
        <header>
            <Header />
        </header>
        <main class="mx-auto max-w-6xl min-h-screen px-3 py-3 rounded-lg bg-white">
            <Messages />
            <Breadcrumb />
            <CookieBanner />
            <slot />
        </main>
        <footer class="mt-3">
            <Footer />
        </footer>
    </section>
</template>
<script setup lang="ts">
import './main.css';
import tracking from '~/util/tracking';
import { useBreadcrumbStore } from '~/stores/breadcrumb';
import Footer from '~/components/Footer.vue';
import Header from '~/components/Header.vue';

const store = useBreadcrumbStore();

onMounted(() => {
    tracking.trackPage()
    store.clear()
});
</script>