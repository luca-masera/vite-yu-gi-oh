<template>
    <div>
        <select name="appsearch" id="appsearch" v-model="text" @change="$emit('searchName', text)">
            <option value="">All</option>
            <option value="Book of">Book of</option>
            <option value="Deskbot">Deskbot</option>
            <option value="Evolsaur">Evolsaur</option>
            <option value="Gadget">Gadget</option>
            <option value="Charmer">Charmer</option>
        </select>

    </div>
</template>

<script>
export default {
    name: 'AppSearch',
    data() {

        return {
            text: ''
        }
    }

}
</script>

<style lang="scss" scoped></style>