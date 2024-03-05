<template>
  <div class="dest-cards">
    <DestCard
      v-for="destination in destinations"
      :key="destination.name"
      :destination="destination"
      :addToCart="addToCart"
    />
    <div class="cart">
      <h2>Cart</h2>
      <ul>
        <li v-for="(item, index) in cart" :key="index">
          <img class="cart-item-image" :src="item.img" :alt="item.name"> <!-- Add mini image -->
          {{ item.name }} - ${{ item.price }}
          <button @click="removeFromCart(index)">Remove</button>
        </li>
      </ul>
      <p>Total: ${{ totalPrice }}</p>
    </div>
  </div>
</template>

<script setup>
import DestCard from "@/components/DestCard.vue";
import { ref, computed } from 'vue';


const destinations = [
  {
    name: "Jordan 4 Black Canvas",
    International: true,
    price: 350,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220711/3c188631bc66495aa0f20423c1ed42d5.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Jordan 4 Frozen Moments",
    International: true,
    price: 300,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20230816/ce5ab4aedb3b4667a21a998c21263c3e.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Jordan 4 Military Black",
    International: true,
    price: 400,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220410/08ca77cb56bc4bad81896ab3533d62df.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  // Add other destinations here
  {
    name: "Jordan 4 Royalty",
    International: false,
    price: 600,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220212/bff9509bd39f464ca370d117cab171c3.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Jordan 4 Metallic Purple",
    International: false,
    price: 600,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220212/466dc6294a5241b7a0c220ba1319c3a7.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Jordan 4 Midnight Navy",
    International: true,
    price: 300,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220806/795e65027cca488b877545fe93cebffb.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Jordan 4 Seafoam",
    International: true,
    price: 450,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20230528/ff23aa7eff334ec5902dc0e588403f67.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Jordan 4 Thunder",
    International: true,
    price: 300,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20230313/e26c03f412264d5c8d92a4476cb865bd.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Jordan 4 Off-White Sail",
    International: true,
    price: 1200,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20230528/d10ce095c253415890a8a4835eb26213.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Jordan 4 Pure Money",
    International: true,
    price: 800,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220212/1178177e58ae44838ce3cb8be8d6d081.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Jordan 4 White Cement",
    International: true,
    price: 550,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220212/7097715027bc42bf8c87112ad44ffdce.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Jordan 4 Oreo",
    International: true,
    price: 420,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220212/61b34cd57533456ea8468575b1e0123e.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
];

const cart = ref([]);

const addToCart = (item) => {
  cart.value.push(item);
};

const removeFromCart = (index) => {
  cart.value.splice(index, 1);
};

// Compute total price
const totalPrice = computed(() => {
  return cart.value.reduce((total, item) => total + item.price, 0);
});
</script>

<style scoped>
.dest-cards {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  justify-content: flex-start;
  gap: 20px;
}

.cart {
  margin-left: auto;
}

.cart h2 {
  margin-bottom: 10px;
}

.cart ul {
  list-style: none;
  padding: 0;
}

.cart li {
  margin-bottom: 5px;
}

.cart-item-image {
  width: 30px; /* Set width of mini image */
  height: 30px; /* Set height of mini image */
  margin-right: 10px; /* Add margin between image and item name */
}

</style>