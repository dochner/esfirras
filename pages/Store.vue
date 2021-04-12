<template>
  <v-container>
    <v-row>
      <v-col sm="3" offset-lg="1">
        <Sidebar />
      </v-col>
      <v-col sm="9" lg="7">
        <ProductDisplay />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
const Sidebar = require('../components/store/Sidebar')
const ProductDisplay = require('../components/store/ProductDisplay')

module.exports = {
  components: {
    Sidebar,
    ProductDisplay
  }
}
</script>
