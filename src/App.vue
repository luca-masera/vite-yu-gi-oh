<template>
  <div>
    <HeaderApp />
    <MainApp />
  </div>
</template>

<script>
import HeaderApp from './components/HeaderApp.vue';
import MainApp from './components/MainApp.vue';
import { store } from './data/store.js';
import axios from 'axios'

export default {
  name: 'App',

  components: {
    HeaderApp,
    MainApp

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
        this.store.cards.push(res.data.data)
        console.log(store.cards)

      })

    }

  },

  created() {
    this.getCards();
  }

}
</script>

<style lang="scss" scoped></style>
{{}}