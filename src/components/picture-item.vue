<template>
  <b-row>
    <b-col sm="12" md="6" lg="6" class="picture-item">
      <img :src="picture.src.medium" />
    </b-col>
    <b-col sm="12" md="6" lg="6" class="header">
      <h1>
        Daily dose of dog
      </h1>
      <p>
        The place to come to get your daily dosage of cute dogs. Built incorporating the pexels api, daily dose of dog finds
        a random image search of a dog on pexels.com. This website is client side so every time you refresh, a new dog will be FETCHED!
      </p>
    </b-col>
  </b-row>


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
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
  .picture-item img{
      width: 90%;
      max-width: 450px;
      max-height: 450px;
  }

  .header{
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    color: #CFCFCF;
  }
</style>
