<!-- <template>
    <main>
        <h1>azzahrascraf_</h1>
        <p>Semua model dan warna hijab juga bahan yang di inginkan ada di sini</p>
    </main>
</template> -->

<script setup>
import TeamCard from '../components/TeamCard.vue'

const daftarTim = [
  { nama: 'Cinta', jabatan: 'Founder & Owner' },
  { nama: 'Aqila', jabatan: 'Kepala Produksi' },
  { nama: 'indira', jabatan: 'Admin & Customer Service' },
]
</script>

<template>
  <div class="about-page">
    <!-- Banner -->
    <section class="banner">
      <h1>Tentang Kami</h1>
    </section>

    <!-- Cerita Kami -->
    <section class="cerita-kami">
      <div class="teks">
        <h2>Cerita Kami</h2>
        <p>
          Toko kami berawal dari sebuah usaha kecil di rumah yang dijalankan
          bersama teman-teman kuliah. Bermula dari hobi, kami mulai menjual
          produk secara online dan perlahan mendapat kepercayaan dari
          pelanggan sekitar kampus. Kini kami terus belajar dan berkembang
          untuk memberikan produk dan pelayanan terbaik.
        </p>
      </div>
      <div class="gambar">
        <img src="https://i.pinimg.com/736x/39/2b/b9/392bb98bb621dab56044fd22a91bc1e6.jpg" alt="Cerita kami" />
      </div>
    </section>

    <!-- Tim Kami -->
    <section class="tim-kami">
      <h2>Tim Kami</h2>
      <div class="grid-tim">
          <TeamCard
          v-for="anggota in daftarTim"
          :key="anggota.nama"
          :nama="anggota.nama"
          :jabatan="anggota.jabatan"
        />
      </div>
    </section>
  </div>
</template>

<style scoped>
.banner {
  background: #ce7fce; /* samakan dengan warna utama landing page */
  color: #efe7f0;
  text-align: center;
  padding: 3rem 1rem;
}

.cerita-kami {
  display: flex;
  align-items: center;
  gap: 2rem;
  padding: 3rem 1.5rem;
  flex-wrap: wrap;
}

.cerita-kami .teks {
  flex: 1;
  min-width: 250px;
}

.cerita-kami .gambar {
  flex: 1;
  min-width: 250px;
  text-align: center;
}

.cerita-kami .gambar img {
  max-width: 100%;
  border-radius: 8px;
}

.tim-kami {
  padding: 3rem 1.5rem;
  text-align: center;
}

.grid-tim {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1.5rem;
  margin-top: 1.5rem;
}
</style>