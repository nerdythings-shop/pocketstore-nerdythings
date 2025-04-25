<template>
  <button class="btn btn-secondary join-item" @click="addToCart(product.id)">
    {{ $t('checkout.add-to-cart') }}
  </button>
</template>

<script lang="ts" setup>
import PocketBase from 'pocketbase';
import { usePocketBase } from '~/util/pocketbase';
import { useLocalStorage } from '@vueuse/core';

const { product } = defineProps({
  product: {
    type: Object, requiered: true
  }
});

const pb = usePocketBase();

const cart = useLocalStorage('cart', [], {});

const addToCart = async (id, qty = 1) => {
  if (!cart.value) {
    cart.value = [];
  }

  // Check if the product already exists in the cart
  const existingItem = cart.value.find(item => item.id === id);

  if (existingItem) {
    // Update quantity if found
    existingItem.qty += qty;
  } else {
    // Fetch product and add it as a new entry
    const product = await pb.collection('products').getOne(id);
    cart.value.push({ id, qty, product });
  }
};
</script>