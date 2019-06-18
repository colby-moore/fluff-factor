<template>
    <b-container fluid class="picture-grid-container">
        <b-row>
            <pictureItem />
            <pictureItem />
            <pictureItem />
            <pictureItem />
            <pictureItem />
            <pictureItem />
            <pictureItem />
            <pictureItem />
        </b-row>
    </b-container>
</template>

<script>
import pictureItem from '../components/picture-item.vue'

export default {
    name: 'pictureGridContainer',
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
