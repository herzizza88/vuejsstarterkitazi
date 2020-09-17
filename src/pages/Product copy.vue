<template>
   <div class="product">
    <div>
      <strong>{{ product1.title }}</strong> - {{ product1.price }}
    </div>

   <div>
        <button @click="addToCart"> Add To Cart</button>
    </div>  
   </div> 
</template>


<script>
export default {
    name: 'Product',
    props: {
        product1: {
            type: Object,
            required: true
        }
    },
    methods: {
        addToCart() {
            this.$store.dispatch('addToCart', this.product)
        }
    }
}
</script>

<style lang="scss">
.product {
  padding: 1rem;
  margin: 1rem 0;
  border: 1px solid #35495e;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>