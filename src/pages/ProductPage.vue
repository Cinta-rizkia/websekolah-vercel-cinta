<script setup>
import ProductCard from '../components/ProductCard.vue'
const daftarProduk = [
 { id: 1, nama: 'Pasmina Viscose', harga: 55000, gambar:
'https://i.pinimg.com/1200x/86/e3/c6/86e3c6313d9ee27ca2724fdf992a04c2.jpg'},
 { id: 2, nama: 'Pasmina Shimer', harga: 76000, gambar:
'https://i.pinimg.com/1200x/af/cd/ae/afcdaeef6c294b86c0169aa0348af948.jpg'},
 { id: 3, nama: 'Segiempat Motif', harga: 60000, gambar:
'https://i.pinimg.com/1200x/c8/ab/4e/c8ab4e7e543bd2300af82ca43dd140e8.jpg'},
 { id: 4, nama: 'Segiempat', harga: 50000, gambar:
'https://i.pinimg.com/1200x/eb/72/db/eb72db9612683957deff7236c7968c1a.jpg'},
]
</script>
<template>
 <main>
 <h1>Produk Kami</h1>
 <div class="grid">
 <ProductCard
 v-for="produk in daftarProduk"
 :key="produk.id"
 :nama="produk.nama"
 :harga="produk.harga"
 :gambar="produk.gambar"
 />
 </div>
 </main>
</template>
<style scoped>
.grid {
 display: flex;
 gap: 16px;
 flex-wrap: wrap;
}
</style>