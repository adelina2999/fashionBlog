<template>
  <v-app>
    <Calculator/>
  </v-app>
</template>

<script>
import Calculator from './components/Calculator/calculator';

export default {
  name: 'App',

  components: {
    Calculator,
  },

  data () {
    return {

    }
  }
}; 
</script>
