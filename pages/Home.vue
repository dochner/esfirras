<template>
  <div>
    <Header />
    <PopularProducts />
    <Footer />
  </div>
</template>

<script>
const Header = require('../components/home/Header')
const PopularProducts = require('../components/home/PopularProducts')
const Footer = require('../components/home/Footer')

module.exports = {
  components: {
    Header,
    PopularProducts,
    Footer
  }
}
</script>
