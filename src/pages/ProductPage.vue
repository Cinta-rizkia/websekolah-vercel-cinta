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
    <div>
        <section class="benner">
        <h1 class="benner-title">Produk Kami</h1>
        <p class="benner-desc">temukan produk yang kalian cari</p>
        </section>
    </div>
    <main>
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
.benner {
    background-color: rgb(250, 209, 248);
    color:#831843;
    text-align: center;
    padding: 60px 20px;
}
.benner-title{
    margin: 0 0 22;
    font-size: 3rem;
}
.benner-decs{
    margin: 0%;
    font-size: 5.5rem;
    opacity: 0.6;
}
.grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  align-items: stretch;
  gap: 16px;
}

@media (min-width: 640px) {
  .grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (min-width: 1024px) {
  .grid {
    grid-template-columns: repeat(4, 1fr);
  }
}
</style>