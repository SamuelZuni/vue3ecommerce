<script lang="ts">
import ProductList from '@/components/ProductList.vue';

export default {
  components: {
    ProductList
  }, 
  props: ['details']
}

</script>

<template>
  <main>
    <ProductList :details="details" />
  </main>
</template>
