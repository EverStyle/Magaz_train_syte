<template>
  <div class="v_cart_hover">
    <h1>Cart</h1>
    <CartItems />
  </div>
</template>

<script>
import CartItems from "@/components/CartItems";
export default {
  name: "Cart",
  components: {
    CartItems
  }
};
</script>
<style>
</style>