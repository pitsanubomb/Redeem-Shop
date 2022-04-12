<template>
  <div class="point">
    <ProductList productType="cash" />
  </div>
</template>

<script>
// @ is an alias to /src
import ProductList from "@/components/ProductList.vue";

export default {
  name: "ProductPoint",
  components: {
    ProductList,
  },
};
</script>
