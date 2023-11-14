<template>
  <HeaderApp />
  <AppSearch @search-name="viewName" />
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
import AppSearch from './components/AppSearch.vue';




export default {
  name: 'App',

  components: {
    HeaderApp,
    MainApp,
    CardMainApp,
    AppSearch

  },
  data() {

    return {
      store,

      params: {
        num: 20,
        offset: 0,
      }

    }

  },

  methods: {

    viewName(resp) {
      console.log(resp)

      if (resp != '') {

        this.params = {
          num: 20,
          offset: 0,
          archetype: resp
        }
      }
      this.getCards()

    },

    getCards() {
      axios.get(store.apiUrl, { params: this.params }).then((res) => {
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