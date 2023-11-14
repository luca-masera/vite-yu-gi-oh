<template>
    <div class=" bg-danger " v-for="(card, index) in store.cards">
        <CardMainApp :name="card.name" :archetype="card.archetype" :images="card.card_images[0].image_url" />


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