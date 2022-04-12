<template>
  <div class="poduct">
    <div class="row">
      <div v-for="p in product" :key="p.id" class="col s12 m4">
        <div class="card">
          <div class="card-image">
            <img
              v-if="!p.imageUrl"
              src="https://www.salonlfc.com/wp-content/uploads/2018/01/image-not-found-scaled-1150x647.png"
            />
            <img v-else :src="p.imageUrl" />
            <span class="card-title">{{ p.productName }}</span>
          </div>
          <div class="card-content">
            <p v-if="productTye === cash">฿{{ p.price }}</p>
            <p v-else>฿{{ p.price }}</p>
          </div>
          <div class="card-action">
            <!-- <a href="#">This is a link</a> -->
          </div>
        </div>
      </div>
    </div>
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
