<template>
  <div class="home">
  <h1>benvenuti</h1>
  jhhgjh
  </div>

  
</template>

<script>
import ut from "../utenti"
export default {
  name: 'HomeView',
  data() {
    return {
      prodotti: [],
      utenti: [],
      loading: false,
      selection: 1,
      downloaded: false,
    }
  },
  methods: {
    getProdotti() {
      fetch('https://dummyjson.com/products')
      .then(res => res.json())
      .then(console.log);
    }
  },
  mounted() {
   this.utenti=ut
 
  }
}
</script>
