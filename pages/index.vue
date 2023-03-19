<template>
  <div>
    <div class="text-center">
      <div class="row">
        <div class="col-4" v-for="i in data" :key="i.id">
          <CardTen :name="i.name" :price="i.price" :img="i.img" :detail="i.detail"/>
        </div>
        <hr />
      </div>
    </div>
  </div>
</template>

<script>
import CardTen from '../components/CardTen.vue';

export default {
    name: "IndexPage",
    components: { CardTen },
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

<style scoped

</style>
