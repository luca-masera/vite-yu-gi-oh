<template>
    <div>
        <img :src="images" :alt="name">
        <h3>{{ name }}</h3>
        <h6>{{ archetype }}</h6>



    </div>
</template>

<script>
import { store } from '../data/store.js';
export default {
    name: 'CardMainApp',


    props: {
        name: String,
        archetype: String,
        images: String,

    },
    data() {

        return {
            store
        }
    }


}
</script>

<style lang="scss" scoped></style>
