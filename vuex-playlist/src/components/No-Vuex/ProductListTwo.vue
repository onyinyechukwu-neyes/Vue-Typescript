<template>
  <div>
    <h2>ProductListTwo</h2>
    <div id="product-list-two">
      <ul>
        <li v-for="(product, index) in products" :key="index">
          <span class="name">{{ product.name }}</span>
          <span class="price">${{ product.price }}</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from "vue";
import { Product } from "../.././types";

export default defineComponent({
  props: {
    products: {
      type: Array as PropType<Product[]>,
      required: true,
    },
  },
  setup() {
    return {};
  },
});
</script>

<style scoped>
#product-list-two {
  background: #d1e4ff;
  box-shadow: 1px 2px 3px rgba(0, 0, 0, 0.2);
  margin-bottom: 30px;
  padding: 10px 20px;
}
#product-list-two ul {
  padding: 0;
  list-style-type: none;
}
#product-list-two li {
  margin-right: 10px;
  margin-top: 10px;
  padding: 20px;
  background: rgba(255, 255, 255, 0.7);
}
.price {
  font-weight: bold;
  color: #860ce8;
  display: block;
}
</style>
