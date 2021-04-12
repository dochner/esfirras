<template>
  <v-card
    outlined
  >
    <v-img
      :src="product.image"
      height="200px"
    />

    <v-card-title>
      {{ product.name }}
    </v-card-title>

    <v-card-subtitle>
      ${{ product.price }}
    </v-card-subtitle>

    <v-card-actions>
      <v-btn
        color="success"
        outlined
        @click="addToCart(i)"
      >
        <v-icon left>fa-plus</v-icon>
        Add to Cart
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
module.exports = {
  props: {
    product: Object,
    addToCart: Function,
    i: Number
  }
}
</script>
