<template>
    <b-container fluid class="picture-grid-container">
        <b-row >
            <pictureItem v-bind:key="pictures.id" v-for="pictures in pictures" v-bind:picture="pictures"/>
        </b-row>
    </b-container>
</template>

<script>
import pictureItem from '../components/picture-item.vue'

export default {
    name: 'pictureGridContainer',
    props: ["pictures"],
    components: {
        pictureItem,
    }
}
</script>

<style>
    .picture-grid-container{
        background-color: gray;
        min-height: 100vh;
    }
</style>
