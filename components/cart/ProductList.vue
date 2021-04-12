<template>
  <div>
    <v-row v-for="(product, i) in $store.state.products" :key="i">
      <HorizontalProduct
        :product="product"
        :i="i"
        :updateCart="removeFromCart"
        btnAction="remove"
      />
    </v-row>
  </div>
</template>

<script>
const HorizontalProduct = require('../cards/HorizontalProduct')

module.exports = {
  components: {
    HorizontalProduct
  },
  methods: {
    removeFromCart() {
    }
  }
}
</script>
