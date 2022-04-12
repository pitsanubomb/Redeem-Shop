<template>
  <div class="hello">
    {{ product }}
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      product: null,
    };
  },
  mounted() {
    const uri = "http://localhost:3000/api/product?productType=" + this.msg;
    fetch(uri)
      .then((res) => res.json())
      .then(({ product }) => (this.product = product));
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
