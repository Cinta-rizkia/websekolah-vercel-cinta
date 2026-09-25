<!-- <template>
    <main>
        <h1>azzahrascraf_</h1>
        <p>Semua model dan warna hijab juga bahan yang di inginkan ada di sini</p>
    </main>
</template> -->
<!-- <script setup>
{jabatan: 'Kepala Produksi'}
{ nama: 'indira, jabatan'}
import TeamCard from '../components/TeamCard.vue'
const daftarTim = [
  { nama: 'Cinta', jabatan: 'Founder & Owner' },
  { nama: 'Aqila', jabatan: 'Admin & Customer Service' },
]
</script>

   <script setup>
<template>
  <div class="about-page"> -->
    <!-- Banner -->
        <!-- <section class="bg-pink-400 h-64 flex items-center justify-center">
      <h1>Tentang Kami</h1>
    </section>
     -->
    <!-- Cerita Kami -->
    <!-- <section class="cerita-kami"> 
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


    <!-- Tim Kami -
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
</script>

<!-- <style scoped>
 .banner{
  background: #ce7fce; 
  color:rgb(250, 248, 249);
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
</style> */ -->
<script setup>
import TeamCard from '../components/TeamCard.vue'

const daftarTim = [
  { nama: 'Cinta', jabatan: 'Founder & Owner' },
  { nama: 'Sabrina', jabatan: 'Admin & Customer Service' },
  { nama: 'Indira', jabatan: 'Kepala Produksi' },
]
</script>

<template>
  <div class="about-page">
    <!-- Banner -->
    <section class="banner">
      <h1>｡:  🎀  𝒯𝑒𝓃𝓉𝒶𝓃𝑔 𝒦𝒶𝓂𝒾  🎀  :｡</h1>
    </section>

    <!-- Cerita Kami -->
    <section class="cerita-kami">
      <div class="teks">
        <h2>🍭  🎀  𝒞𝑒𝓇𝒾𝓉𝒶 𝒦𝒶𝓂𝒾  🎀  🍭</h2>
        <p>
          𝐓𝐨𝐤𝐨 𝐤𝐚𝐦𝐢 𝐛𝐞𝐫𝐚𝐰𝐚𝐥 𝐝𝐚𝐫𝐢 𝐬𝐞𝐛𝐮𝐚𝐡 𝐮𝐬𝐚𝐡𝐚 𝐤𝐞𝐜𝐢𝐥 𝐝𝐢 𝐫𝐮𝐦𝐚𝐡 𝐲𝐚𝐧𝐠 
          𝐝𝐢𝐣𝐚𝐥𝐚𝐧𝐤𝐚𝐧 𝐛𝐞𝐫𝐬𝐚𝐦𝐚 𝐭𝐞𝐦𝐚𝐧-𝐭𝐞𝐦𝐚𝐧 𝐤𝐮𝐥𝐢𝐚𝐡. 𝐁𝐞𝐫𝐦𝐮𝐥𝐚 𝐝𝐚𝐫𝐢 𝐡𝐨𝐛𝐢,
           𝐤𝐚𝐦𝐢 𝐦𝐮𝐥𝐚𝐢 𝐦𝐞𝐧𝐣𝐮𝐚𝐥 𝐩𝐫𝐨𝐝𝐮𝐤 𝐬𝐞𝐜𝐚𝐫𝐚 𝐨𝐧𝐥𝐢𝐧𝐞 𝐝𝐚𝐧 𝐩𝐞𝐫𝐥𝐚𝐡𝐚𝐧
            𝐦𝐞𝐧𝐝𝐚𝐩𝐚𝐭 𝐤𝐞𝐩𝐞𝐫𝐜𝐚𝐲𝐚𝐚𝐧 𝐝𝐚𝐫𝐢 𝐩𝐞𝐥𝐚𝐧𝐠𝐠𝐚𝐧 𝐬𝐞𝐤𝐢𝐭𝐚𝐫 𝐤𝐚𝐦𝐩𝐮𝐬. 𝐊𝐢𝐧𝐢
             𝐤𝐚𝐦𝐢 𝐭𝐞𝐫𝐮𝐬 𝐛𝐞𝐥𝐚𝐣𝐚𝐫 𝐝𝐚𝐧 𝐛𝐞𝐫𝐤𝐞𝐦𝐛𝐚𝐧𝐠 𝐮𝐧𝐭𝐮𝐤 𝐦𝐞𝐦𝐛𝐞𝐫𝐢𝐤𝐚𝐧 𝐩𝐫𝐨𝐝𝐮𝐤 𝐝𝐚𝐧 
             𝐩𝐞𝐥𝐚𝐲𝐚𝐧𝐚𝐧 𝐭𝐞𝐫𝐛𝐚𝐢𝐤.

        </p>
      </div>
      <div class="gambar">
        <img
          src="https://i.pinimg.com/736x/39/2b/b9/392bb98bb621dab56044fd22a91bc1e6.jpg"
          alt="Cerita kami"
        />
      </div>
    </section>

    <!-- Tim Kami -->
    <section class="tim-kami">
      <h1>🐇  🎀  𝒯𝐼𝑀 𝒦𝒜𝑀𝐼  🎀  🐇</h1>
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
  background: rgb(250, 209, 248);
  color:#831843;
  text-align: center;
  padding: 3rem;
  font-size:60px;
}

.cerita-kami {
  display: flex;
  align-items: center;
  gap: 2rem;
  padding: 3rem;
  flex-wrap: wrap;
}

.cerita-kami .teks {
  flex: 1;
  min-width: 250px;
  color: #831843;
  font-size:15x;
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
  font-size: 40px;
  color: #831843;
}

.grid-tim {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1.5rem;
  margin-top: 1.5rem;
}
</style>