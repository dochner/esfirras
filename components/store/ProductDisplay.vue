<template>
  <div>
    <h3>Products</h3>

    <v-row>
      <v-col
        sm="6"
        md="4"
        v-for="(product, i) in $store.state.products"
        :key="product.name"
      >
        <VerticalProduct :product="product" :i="i" :addToCart="addToCart" />
      </v-col>
    </v-row>
  </div>
</template>

<script>
const VerticalProduct = require('../cards/VerticalProduct')

module.exports = {
  components: {
    VerticalProduct
  },
  methods: {
    addToCart(index, quantity = 1) {
      this.$store.commit('addItemToCart', { itemId: index, quantity })
      this.$store.commit('updateSnackbar', { show: true })
    }
  }
}
</script>
