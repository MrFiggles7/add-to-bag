<template>
  <div id="app">
      <add-to-cart-button :item="item" @add-to-cart="addToCart"></add-to-cart-button>
      <cart :cart="cart"></cart>
  </div>
</template>

<script>

import Cart from "@/components/Cart";
import AddToCartButton from "@/components/AddToCartButton";
export default {
  name: 'App',
  components: {
    AddToCartButton,
    Cart
  },

  data(){

    return{
      item: {
        name: 'ItemName',
        price: 2.99
      },

      cart: [],
    }

  },

  methods: {
    addToCart: function (item) {
        this.cart.push(item);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
