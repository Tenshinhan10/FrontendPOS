<template>
  <div><h1>{{title}}</h1>
  <p>{{ someText }}</p>
  name : {{ data.name }} <br>
  age : {{ data.age }}
  <CardTen /></div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return{
        title : "University 2222",
        someText : "test",
    };
  },
  mounted(){
    console.log("mountes load success!");
    this.someText = 'ten';
  },
  created(){
    console.log("created eiei");
    this.data = {
        name : 'sss',
        age : 10,
    }
  },
};
</script>

<style scoped>
.h1 {
    color: blue;
}

</style>
