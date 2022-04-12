<template>
  <div class="poduct">
    {{ product }}
  </div>
</template>

<script>
export default {
  name: "ProductList",
  props: {
    productType: String,
  },
  data() {
    return {
      product: null,
    };
  },
  mounted() {
    const uri =
      "http://localhost:3000/api/product?productType=" + this.productType;
    fetch(uri)
      .then((res) => res.json())
      .then(({ product }) => (this.product = product));
  },
};
</script>
