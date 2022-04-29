<template>
  <div>
    <h1>Your Cart</h1>

    <CartItemCard
      v-for="product in items"
      :key="product.id"
      :product="product"
    />
    <CartSummaryPaymentCart />
  </div>
</template>

<script>
import CartItemCard from "../components/cart-page/CartItemCard.vue";
import CartSummaryPaymentCart from "../components/cart-page/CartSummaryPaymentCart.vue";
export default {
  components: { CartItemCard, CartSummaryPaymentCart },
  computed: {
    items() {
      return this.$store.getters.cartItems;
    },
  },
};
</script>

<style>
</style>