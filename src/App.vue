<template>
  <HeaderApp />
  <div class="container  d-flex flex-wrap ">
    <MainApp />
  </div>

  <CardMainApp />
</template>

<script>
import CardMainApp from './components/CardMainApp.vue';
import HeaderApp from './components/HeaderApp.vue';
import MainApp from './components/MainApp.vue';
import { store } from './data/store.js';
import axios from 'axios'



export default {
  name: 'App',

  components: {
    HeaderApp,
    MainApp,
    CardMainApp
  },
  data() {

    return {
      store
    }

  },

  methods: {
    getCards() {
      axios.get(store.apiUrl).then((res) => {
        console.log(res)
        console.log(res.data.data)
        store.cards = (res.data.data)
        console.log(store.cards)


      })

    }

  },

  created() {
    this.getCards();
  }

}
</script>

<style lang="css" scoped></style>
{{}}