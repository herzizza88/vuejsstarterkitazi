<template>
    <main class="products">
        <ul>
            <li v-for="(prod,index) in products" :key="index">
            <Product :product1="prod" />
           </li>
        </ul>
    </main>
</template>

<script>
import Product from './Product.vue'

export default {
    name: 'Products',      
    components: {
        Product
    },
    computed: {
        products() {
            return this.$store.getters.products
        }
    }

}
</script>