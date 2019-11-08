<template>
  <v-app>
    <Header/>
    <Calculator/>
    <Layout/>
    <Footer/>
  </v-app>
</template>

<script>
import Header from './components/Header/header';
import Calculator from './components/Calculator/calculator';
import Layout from './components/Layout/layout';
import Footer from './components/Footer/footer';

export default {
  name: 'App',

  components: {
    Header,
    Calculator,
    Layout,
    Footer,

  },

  data () {
    return {

    }
  }
}; 
</script>
