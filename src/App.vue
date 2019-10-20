<template>
  <div id="app" class="background-img">
    <Header />
    <Layout />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header/header.vue'
import Footer from './components/Footer/footer.vue'
import Layout from './components/Layout/layout.vue'

export default {
  name: 'app',
  components: {
    Header,
    Footer,
    Layout
  }
}
</script>

<style>
.background-img {
  background-image:url('./assets/background.jpg');
	text-align: center;
}
</style>
