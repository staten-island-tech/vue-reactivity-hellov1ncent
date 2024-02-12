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
    name: "Travis Scott Golf",
    Instock: true,
    price: 800,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20231008/a1b6bb2834534a37b3687329578e30ac.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Kobe 5 Bruce Lee",
    Instock: true,
    price: 800,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220212/c8402033bcd246eb933275091ce8c06a.jpg?x-oss-process=image/format,webp/resize,w_800",
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
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20230528/373224f4eb5e47fea4f38e1c15bffd00.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Fragment X Travis Scott",
    International: true,
    price: 800,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20230528/6672f36dcc88496e8db36e847f51b988.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Jordan 4 Red Cement",
    International: true,
    price: 800,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20230528/799461d9d30e459492fa97b67845b42f.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Yeezy Slide Bone",
    International: true,
    price: 800,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20230805/6dc4ae93c7f64ab2839c59c37b3e82f2.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Yeezy Slide Onyx",
    International: true,
    price: 800,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20230601/4e50fa8b7225434fa5f98628ed2383ef.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Jordan 3 White Cement Reimagined",
    International: true,
    price: 800,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20230222/690e88c4448f44138def735660576034.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Aj1 Retro High Dior",
    International: true,
    price: 800,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220212/b963940873d54184bdcea2230bd4fd11.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Aj1 Obsidian",
    International: true,
    price: 800,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220212/3eaca4dcdbe047c89f6fac15738fdb53.jpg?x-oss-process=image/format,webp/resize,w_800",
  },
  {
    name: "Aj1 Mocha",
    International: true,
    price: 800,
    img: "https://cdn-img.poizonapp.com/pro-img/cut-img/20220212/72f49fd67777448a90cb94fbdc62de4b.jpg?x-oss-process=image/format,webp/resize,w_800",
  },





];
</script>

<style scoped></style>