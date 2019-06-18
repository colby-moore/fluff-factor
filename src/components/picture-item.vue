<template>
  <b-col sm="12" md="4" lg="3" class="picture-item">
    <img :src="picture.src.medium" />
    <h6>{{ picture.id }}</h6>
  </b-col>
</template>

<script>
export default {
  name: 'pictureItem',
  props: ["picture"],
  // props: ['pictures'],
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
