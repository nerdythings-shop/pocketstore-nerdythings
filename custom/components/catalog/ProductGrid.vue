<template>
    <div v-for="product in products" :key="product.id" class="col-span-6 md:col-span-2 py-3">
        <CatalogProductCard :identifier="product.id" />
    </div>
</template>

<script setup>
import PocketBase from 'pocketbase';
import { usePocketbaseStore } from '~/stores/pocketbase';

const { categoryName } = defineProps({
    categoryName: { type: String, required: true }
});

const store = usePocketbaseStore();
const { url } = storeToRefs(store);
const pb = new PocketBase(url.value);
const category = ref({});
const products = ref([]);

onMounted(async () => {
    category.value = await pb.collection('categories').getFirstListItem('slug="' + categoryName + '"');
    console.log(url.value);
    products.value = (await pb.collection('products').getList(1,9, {filter: 'category.slug = "bowling"'})).items;
});
</script>
