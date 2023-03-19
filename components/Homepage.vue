<template>
  <div>
    <div class="container">
  <b-card
    :title="name"
    :img-src="img"
    img-alt="Image"
    img-top
    tag="article"
    class="mb-2"
  >
    <b-card-text>
      รายละเอียด : {{ detail }} <br>
      ราคา : {{ price }} ฿
    </b-card-text>
    <b-button href="#" variant="secondary">Delete</b-button>
    <b-button href="#" variant="secondary">Edit</b-button>
  </b-card>
</div>
</div>
</template>

<script>
export default {
  props:{
  price:{
    type: Number,
    default:0,
  },
  name:{
    type: String,
    default:"",
  },
  img:{
    type: String,
    default:"",
  },
  detail:{
    type: String,
    default:"",
  }
  }
}
</script>

<style>
.nuxt-logo {
  height: 180px;
}
</style>
