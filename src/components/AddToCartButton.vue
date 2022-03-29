<template>
    <div>
        <h6>My Object</h6>
        <div>Name: {{item.name}}</div>
        <div>Price: ${{item.price}}</div>
        <button @click="addToCart(item)">Add To Cart</button>
    </div>

</template>

<script>
    export default {
        name: "AddToCartButton",

        props: {
            item: Object,
        },

        methods: {
            addToCart: function (item) {
                this.$emit('add-to-cart', item)
            }
        }
    }
</script>

<style scoped>

</style>
