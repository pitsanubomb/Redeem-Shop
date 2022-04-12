<template>
  <div class="point">
    <ProductList productType="point" />
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
