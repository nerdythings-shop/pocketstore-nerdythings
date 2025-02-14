<template>
    <section class="min-h-screen bg-cover bg-fixed">
        <header class="py-3">
            <Header />
        </header>
        <main class="mx-auto max-w-6xl min-h-screen px-3 py-3 rounded-lg bg-white">
            <Messages />
            <Breadcrumb />
            <Sections />
            <CookieBanner />
            <slot />
        </main>
        <footer class="mt-3">
            <Footer />
        </footer>
    </section>
</template>
<script setup lang="ts">
import "./main.css";
import tracking from "~/util/tracking";
import { useBreadcrumbStore } from "~/stores/breadcrumb";
import Footer from "~/components/Footer.vue";
import Header from "~/components/Header.vue";
import Sections from "../components/Sections.vue";

const store = useBreadcrumbStore();

onMounted(() => {
    tracking.trackPage();
    store.clear();
});
</script>

<style>
section.bg-cover {
    background:
        radial-gradient(black 15%, transparent 16%) 0 0,
        radial-gradient(black 15%, transparent 16%) 8px 8px,
        radial-gradient(rgba(255, 255, 255, .1) 15%, transparent 20%) 0 1px,
        radial-gradient(rgba(255, 255, 255, .1) 15%, transparent 20%) 8px 9px;
    background-color: #282828;
    background-size: 16px 16px;
}
</style>
