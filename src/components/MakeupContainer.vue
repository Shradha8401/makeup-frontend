<template>
 
  <div v-if="products.length !== 0">
    <div id="product-cont">
      <div v-for="product in products" :key="product.id">
        <!-- <p>{{ product}}-->
        <MakeupComp :product="product" />
      </div>
    </div>
  </div>
  <div v-else>
    <h1>No Data Found.</h1>
  </div>
</template>

<script>
import MakeupComp from "./MakeupComp.vue";
// import db from './../../db.json';

export default {
  name: "MakeupContainer",
  props: [],
  data() {
    return {
      products: [],
    };
  },
  components: {
    MakeupComp,
  },
  async created() {
    const res = await fetch("https://makeup-backend2.onrender.com/api");
    const data = await res.json();
    console.log(data);
    this.products = data;
  },
};
</script>

<style scoped>
#product-cont {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-evenly;
  align-items: center;
}
</style>
