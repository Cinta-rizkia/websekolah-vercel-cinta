<script setup>
import { ref } from 'vue'

defineProps(['nama', 'harga', 'gambar'])

const gambarDipilih = ref(null)

function bukaPreview(src) {
  gambarDipilih.value = src
}

function tutupPreview() {
  gambarDipilih.value = null
}

function tambahKeKeranjang(nama) {
  const suara = new Audio('/nikin-pop-up-something-160353.mp3')
  suara.play().catch(() => {})
  alert(`${nama} ditambahkan ke keranjang!`)
}
</script>

<template>
  <article class="kartu-produk">
    <!-- Foto produk (klik untuk memperbesar) -->
    <button
      type="button"
      :aria-label="`Perbesar foto ${nama}`"
      class="tombol-foto"
      @click="bukaPreview(gambar)"
    >
      <img :src="gambar" :alt="nama" loading="lazy" class="gambar-produk" />
      <span class="ikon-zoom">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="svg-kecil">
          <path stroke-linecap="round" stroke-linejoin="round" d="m21 21-5.197-5.197m0 0A7.5 7.5 0 1 0 5.196 5.196a7.5 7.5 0
           0 0 10.607 10.607ZM10.5 7.5v6m3-3h-6" />
        </svg>
      </span>
    </button>

    <!-- Info produk -->
    <div class="info-produk">
      <h3 class="nama-produk">{{ nama }}</h3>
      <p class="harga-produk">Rp {{ harga.toLocaleString('id-ID') }}</p>

      <button type="button" class="tombol-keranjang" @click="tambahKeKeranjang(nama)">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="svg-sedang">
          <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383
           1.437M7.5 14.25a3 3 0 0 0-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114
            0 0 0-16.536-1.84M7.5 14.25 5.106 5.272M6 20.25a.75.75 0 1 1-1.5 0 .75.75 0 0 1 1.5 0Zm12.75 0a.75.75 0 1 1-1.5 0 
            .75.75 0 0 1 1.5 0Z" />
        </svg>
        Tambah ke Keranjang
      </button>
    </div>
  </article>

  <Teleport to="body">
    <Transition name="fade">
      <div v-if="gambarDipilih" class="overlay-preview" @click="tutupPreview">
        <button type="button" aria-label="Tutup preview" class="tombol-tutup" @click.stop="tutupPreview">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="svg-sedang">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
          </svg>
        </button>
        <img :src="gambarDipilih" :alt="nama" class="gambar-preview" />
      </div>
    </Transition>
  </Teleport>
</template>

<style scoped>
.kartu-produk {
  display: grid;
  grid-template-rows: auto 1fr;
  height: 100%;
  overflow: hidden;
  border: 1px solid #fbcfe8;
  border-radius: 1rem;
  background: #fff;
  box-shadow: 0 1px 3px rgba(244, 114, 182, 0.15);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.kartu-produk:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 20px rgba(244, 114, 182, 0.25);
}

.tombol-foto {
  position: relative;
  display: block;
  width: 100%;
  aspect-ratio: 1 / 1;
  overflow: hidden;
  background: #fdf2f8;
  border: none;
  padding: 0;
  margin: 0;
  cursor: zoom-in;
  flex-shrink: 0;
}

.tombol-foto:focus-visible {
  outline: 3px solid #f9a8d4;
  outline-offset: 2px;
}

.gambar-produk {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.kartu-produk:hover .gambar-produk {
  transform: scale(1.05);
}

.ikon-zoom {
  position: absolute;
  top: 0.5rem;
  right: 0.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2rem;
  height: 2rem;
  border-radius: 9999px;
  background: rgba(255, 255, 255, 0.9);
  color: #ec4899;
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.15);
  opacity: 0;
  transition: opacity 0.2s ease;
}

.kartu-produk:hover .ikon-zoom {
  opacity: 1;
}

/* Info produk: 3 baris tetap (nama, harga, tombol) supaya antar kartu sejajar rapi */
.info-produk {
  display: grid;
  grid-template-rows: auto auto 1fr;
  gap: 0.5rem;
  padding: 1rem;
  text-align: center;
}

.nama-produk {
  min-height: 2.5rem;
  font-size: 1rem;
  font-weight: 600;
  line-height: 1.35;
  color: #831843;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

.harga-produk {
  font-size: 1rem;
  font-weight: 700;
  color: #ec4899;
}

.tombol-keranjang {
  align-self: end;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  width: 100%;
  border: none;
  border-radius: 9999px;
  background: #fbcfe8;
  color: #831843;
  padding: 0.65rem 1rem;
  font-size: 0.875rem;
  font-weight: 600;
  cursor: pointer;
  transition: background 0.15s ease, transform 0.1s ease;
}

.tombol-keranjang:hover {
  background: #f9a8d4;
}

.tombol-keranjang:active {
  transform: scale(0.95);
}

.tombol-keranjang:focus-visible {
  outline: 3px solid #f9a8d4;
  outline-offset: 2px;
}

.svg-kecil {
  width: 1rem;
  height: 1rem;
}

.svg-sedang {
  width: 1.25rem;
  height: 1.25rem;
}

/* Overlay preview gambar */
.overlay-preview {
  position: fixed;
  inset: 0;
  z-index: 50;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(80, 7, 36, 0.6);
  backdrop-filter: blur(4px);
  padding: 1rem;
  cursor: zoom-out;
}

.tombol-tutup {
  position: absolute;
  top: 1rem;
  right: 1rem;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2.5rem;
  height: 2.5rem;
  border: none;
  border-radius: 9999px;
  background: rgba(255, 255, 255, 0.9);
  color: #db2777;
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.2);
  cursor: pointer;
  transition: background 0.15s ease;
}

.tombol-tutup:hover {
  background: #fff;
}

.gambar-preview {
  max-height: 85vh;
  max-width: 90vw;
  border-radius: 1.5rem;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
  outline: 4px solid rgba(255, 255, 255, 0.7);
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.2s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>