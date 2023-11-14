<template>
    <div>
        <CardMainApp v-for="card in store.cards" :name="card.name" :archetype="card.archetype" :images="card.card_images" />



    </div>
</template>

<script>
import { store } from '../data/store.js';
import CardMainApp from './CardMainApp.vue';

export default {
    name: 'MainApp',

    components: {
        CardMainApp

    },
    data() {

        return {
            store
        }
    }



}
</script>

<style lang="scss" scoped></style>