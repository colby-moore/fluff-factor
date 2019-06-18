<template>
  <b-col sm="12" md="4" lg="3" class="picture-item">
    <img src="https://images.pexels.com/photos/1254140/pexels-photo-1254140.jpeg?auto=format%2Ccompress&cs=tinysrgb&dpr=2&h=650&w=940" />
  </b-col>
</template>

<script>
export default {
  name: 'pictureItem',
}
</script>

<style scoped>
  .picture-item{
    margin-bottom: 40px;
  }
  .picture-item img{
    width: 100%;
  }
</style>
