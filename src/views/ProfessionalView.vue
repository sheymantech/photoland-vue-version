<script setup>
import ProductCategory from '../components/ProductCategory.vue'
import { useProductsStore } from '@/stores/products'

const productsStore = useProductsStore()

const professionalProduct = productsStore.products.filter(
  (product) => product.category === 'PROFESSIONAL'
)
</script>

<template>
  <ProductCategory :productCategory="professionalProduct" />
</template>
