<script lang="ts">
import Cart from '@/components/Cart.vue';

export default {
  components: {
    Cart
  },
  props: ['details']
}
</script>
<template>
    <div class="about">
      <Cart :details="details"/>
  </div>
</template>