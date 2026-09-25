<script setup>
// Form ini masih tampilan saja, belum ada logic submit
</script>

<template>
  <div class="contact-page">
    <!-- Banner -->
    <section class="banner">
      <h1>🍫  🎀  𝐻𝓊𝒷𝓊𝓃𝑔𝒾 𝒦𝒶𝓂𝒾  🎀  🍫</h1>
    </section>

    <!-- Info Kontak & Formulir -->
    <section class="contact-content">
      <div class="info-kontak">
        <h2>Info Kontak</h2>
        <p>📍 Jl.Banda Asri. KP.Sindang Palay</p>
        <p>📞 0838-3616-5765</p>
        <p>✉️ @azzahrascraf_</p>
        <p>🕒 Senin – Sabtu, 09.00 – 17.00</p>
      </div>

      <div class="formulir">
        <h2>Kirim Pesan</h2>
        <form>
          <div class="field">
            <label for="nama">Nama</label>
            <input id="nama" type="text" placeholder="Nama lengkap kamu" />
          </div>

          <div class="field">
            <label for="email">Email</label>
            <input id="email" type="email" placeholder="nama@email.com" />
          </div>

          <div class="field">
            <label for="pesan">Pesan</label>
            <textarea id="pesan" rows="4" placeholder="Tulis pesan kamu di sini..."></textarea>
          </div>

          <button type="button">Kirim</button>
        </form>
      </div>
    </section>
  </div>
</template>

<style scoped>
.banner {
  background:rgb(250, 209, 248); /* samakan dengan warna Landing Page & About Page */
  color: #831843;
  text-align: center;
  padding: 3rem 1rem;
  font-size: 95px;
}

.contact-content {
  display: flex;
  gap: 2rem;
  padding: 3rem 1.5rem;
  flex-wrap: wrap;
}

.info-kontak {
  flex: 1;
  min-width: 250px;
}

.info-kontak p {
  margin: 0.75rem 0;
  font-size: 1rem;
}

.formulir {
  flex: 1;
  min-width: 280px;
  background: #fff;
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
}

.field {
  margin-bottom: 1rem;
  display: flex;
  flex-direction: column;
}

.field label {
  margin-bottom: 0.4rem;
  font-weight: 600;
  font-size: 0.9rem;
}

input,
textarea {
  padding: 0.6rem 0.8rem;
  border-radius: 8px;
  border: 1px solid #181717;
  font-family: inherit;
  font-size: 0.95rem;
}

input:focus,
textarea:focus {
  outline: none;
  border-color: #f5eef4;
}

button {
  background: #da9ae793;
  color: #fff;
  border: none;
  padding: 0.7rem 2rem;
  border-radius: 999px;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  margin-top: 0.5rem;
}

button:hover {
  opacity: 0.9;
}
</style>