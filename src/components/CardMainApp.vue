<template>
    <div>
        <img :src="image" :alt="name">
        <h3>{{ name }}</h3>
        <h6>{{ archeotype }}</h6>

    </div>
</template>

<script>

export default {
    name: 'CardMainApp',


    props: {
        name: String,
        archeotype: String,
        image: String
    }


}
</script>

<style lang="scss" scoped></style>
