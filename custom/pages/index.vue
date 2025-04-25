<script setup>
import HeroWelcome from '~/components/hero/welcome';
import HeroSales from '~/components/hero/sales';
</script>

<template>
    <section class="page">
        <div class="mx-auto max-w-6xl grid grid-cols-6 gap-3 mt-3">
            <div class="col-span-6 md:col-span-3">
                <section class="alert alert-success flex justify-center">
                    <p class="text-sm font-bold text-white">Dies ist eine Demo Store von <a
                            href="https://www.pocketstore.io" class="text-red-600">PocketStore.io</a></p>
                </section>
            </div>
            <div class="col-span-6 md:col-span-3">
                <section class="alert alert-warning flex justify-center">
                    <p class="text-sm font-bold text-white">Dieser Shop ist nur zum Test online, keine
                        Verkäufe.
                    </p>
                </section>
            </div>
            <div class="col-span-6 md:col-span-3">
                <HeroWelcome />
            </div>
            <div class="col-span-6 md:col-span-3">
                <HeroSales />
            </div>
            <CatalogProductGrid category-name="bowling" />
        </div>
    </section>
</template>