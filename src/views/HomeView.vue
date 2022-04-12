<template>
  <div class="home">
    <ProductList productType="cash" />
  </div>
</template>

<script>
// @ is an alias to /src
import ProductList from "@/components/ProductList.vue";

export default {
  name: "ProductCash",
  components: {
    ProductList,
  },
};
</script>
