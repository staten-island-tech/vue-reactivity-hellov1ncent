<template>
  <div>
    <DestCard
      v-for="destination in destinations"
      :key="destination.name"
      :Destination="destination"
    />
  </div>
</template>

<script setup>
import DestCard from "@/components/icons/destcard.vue";
const destinations = [
  {
    name: "Aj1 Lost and Found",
    InStock: true,
    price: 1300,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20221114/9be86c8d5d0944ebaec1bb1bad43c7f3.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Aj1 UNC",
    Instock: true,
    price: 800,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220212/f706a17ef17242f4baa51d34f77ee618.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Jordan 4 Midnight Navy",
    Instock: true,
    price: 1200,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220806/795e65027cca488b877545fe93cebffb.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Jordan 4 Military Black",
    Instock: false,
    price: 900,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220410/08ca77cb56bc4bad81896ab3533d62df.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Grey Fog Dunks",
    Instock: false,
    price: 400,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20230721/e9de9d6270304edf99b3f4c33925f601.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Michigan State Dunks",
    Instock: true,
    price: 800,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220811/0acd26377315474ebcb5b1de8ffc62a4.png?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Kobe Protro 6 All Star",
    Instock: true,
    price: 800,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20230526/d9e9a4c91b024243a16dbfa69fd21e30.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Kobe Protro 6 Mambacita",
    Instock: true,
    price: 800,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220428/8e6f51bea872465aac88b03ca5f182c0.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Travis Scott Phantom",
    Instock: true,
    price: 800,
    img: "https://images.stockx.com/images/Air-Jordan-1-Retro-Low-OG-SP-Travis-Scott-Black-Phantom-Product.jpg?fit=fill&bg=FFFFFF&w=700&h=500&fm=webp&auto=compress&q=90&dpr=2&trim=color&updated_at=1671732011",
  },
  {
    name: "Kobe 5 Bruce Lee",
    Instock: true,
    price: 800,
    img: "https://shopprimereps.com/cdn/shop/products/nike-kobe-5-protro-x-bruce-lee-287812.jpg?v=1697049768&width=1445",
  },
  {
    name: "Kobe Protro 6 Grinch",
    Instock: true,
    price: 800,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220212/467bfd10065844b788a1e6c12e277675.jpg?x-oss-process=image/format,webp",
  },
  {
    name: "Travis Scott Reverse Mocha",
    International: true,
    price: 800,
    img: "https://sneakerbardetroit.com/wp-content/uploads/2022/05/Travis-Scott-Air-Jordan-1-Low-OG-Reverse-Mocha-DM7866-162-Release-Date-4.jpeg",
  },
  {
    name: "Fragment X Travis Scott",
    International: true,
    price: 800,
    img: "https://sneakerbardetroit.com/wp-content/uploads/2021/07/Travis-Scott-Fragment-Air-Jordan-1-Low-DM7866-140-Release-Date-4-1068x660.jpg",
  },
  {
    name: "MSCHF RED BOOTS",
    International: true,
    price: 800,
    img: "",
  },
  {
    name: "Yeezy Slide Bone",
    International: true,
    price: 800,
    img: "https://images.unsplash.com/photo-1473580044384-7ba9967e16a0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80&quot;",
  },
  {
    name: "Yeezy Slide Onyx",
    International: true,
    price: 800,
    img: "https://images.unsplash.com/photo-1473580044384-7ba9967e16a0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80&quot;",
  },
  {
    name: "Jordan 3 White Cement Reimagined",
    International: true,
    price: 800,
    img: "https://images.unsplash.com/photo-1473580044384-7ba9967e16a0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80&quot;",
  },
  {
    name: "Aj1 Retro High Dior",
    International: true,
    price: 800,
    img: "https://images.unsplash.com/photo-1473580044384-7ba9967e16a0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80&quot;",
  },
  {
    name: "Aj1 Off-White Chicago",
    International: true,
    price: 800,
    img: "https://images.unsplash.com/photo-1473580044384-7ba9967e16a0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80&quot;",
  },
  {
    name: "Lightning Mcqueen Crocs",
    International: true,
    price: 800,
    img: "https://images.unsplash.com/photo-1473580044384-7ba9967e16a0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80&quot;",
  },





];
</script>

<style scoped></style>