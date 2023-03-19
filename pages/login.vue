<template>
  <div>
    <div class="text-center">
      <div><br><b-button href="#" variant="secondary" class="text-right">Add Product</b-button>
      </div><br>
      <div class="row">
        <div class="col-4" v-for="i in data" :key="i.id">
          <Homepage :name="i.name" :price="i.price" :img="i.img" :detail="i.detail"/>
        </div>
        <hr />
      </div>
    </div>
  </div>
</template>

<script>
import Homepage from '../components/Homepage.vue';

export default {
  name: "IndexPage",
  components: { Homepage },
    layout : "default", 
    data() {
    return {
      data: [],
    };
  },
  mounted() {
    this.getData();
  },
  methods: {
    async getData() {
      const { data } = await this.$axios.get();
      this.data = data;
    },
  }, 
};
</script>

<style scoped></style>
