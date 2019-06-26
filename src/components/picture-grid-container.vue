<template>
    <b-container class="picture-grid-container">

        <pictureItem v-bind:key="pictures.id" v-for="pictures in pictures" v-bind:picture="pictures"/>

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
        align-items: center;    
        background: #242A2F;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        min-height: 65vh;
        width: 70%;
        -webkit-box-shadow: 2px 0px 47px 2px rgba(0,0,0,0.75);
        -moz-box-shadow: 2px 0px 47px 2px rgba(0,0,0,0.75);
        box-shadow: 2px 0px 47px 2px rgba(0,0,0,0.75);
        border-radius: 8px;
    }

    .picture-grid-container .row{  
        min-height: 65vh;
    }
</style>
