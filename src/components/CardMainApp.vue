<template>
    <div class="d-flex flex-column align-items-center m-3 box ">

        <img :src="images" :alt="name">
        <h5>{{ name }}</h5>
        <h5>{{ archetype }}</h5>

    </div>
</template>

<script>
import { store } from '../data/store.js';
export default {
    name: 'CardMainApp',


    props: [
        'name',
        'archetype',
        'images'

    ]

    ,
    data() {

        return {
            store
        }
    }


}
</script>

<style lang="css" scoped>
img {
    width: 150px;
}

.box {
    height: 300px;
    width: 250px;
    background-color: aqua;

}
</style>
