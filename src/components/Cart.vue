<template>
    <div>
        <div>Cart:</div>
        <ul>
            <li v-for="item in cart" :key="item.id" style="list-style: none">
                <div>
                    Name:{{item.name}}<br>
                    Price: ${{item.price}}
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: "Cart",

        props: {
            cart: Array,
        }
    }


</script>

<style scoped>

</style>
