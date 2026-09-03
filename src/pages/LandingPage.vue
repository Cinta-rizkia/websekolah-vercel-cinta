<template>
  <div class="landing">
   
    <section class="hero bg-indigo-500 p-[100px] flex-col items-center text-center text-white gap-[18px]">
      <h1 class="text-[62pt] text-center">Tersedia semua jenis hijab</h1>
      <p class="text-[28pt] landing-[80pt]">cari hijab apa?semua ada disini mulai dari warna model semuanya ada</p>
<button
      class="mb-8 mt-[40px] text-[24pt] bg-white text-indigo-500 px-[40px] py-[10px] rounded-4xl transition duration-150 hover:bg-blue-200 active:scale-95">
      <router-link to="/product" class="hero-btn">Lihat Produk</router-link>
    </button>
      <center>
      <video controls width="480" loop>
 <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4" />
      </video>
    </center>
    </section>
    
    
    
    <section class="features">
      <div class="card">
        <span class="card-icon">✔️</span>
        <h3>Kualitas Terjamin</h3>
        <p>Bahan danwarna pilih sendiri</p>
      </div>
      <div class="card">
        <span class="card-icon">💰</span>
        <h3>Harga Bersahabat</h3>
        <p>Harga terjangkau </p>
      </div>
      <div class="card">
        <span class="card-icon">🏩</span>
        <h3>Ambil hijab di ofline store</h3>
        <p>Tidak perlu ongkir</p>
      </div>
    </section>
    
    <!-- FOOTER -->
    <footer class="footer">
      <p>azzahrascraf_</p>
    </footer>
  </div>
</template>

<script>
import { getCurrentWatcher } from 'vue';

export default {
  name: 'LandingPage'
}
</script>

<style scoped>
/* NAVBAR */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 16px 32px;
  background-color: #ffffff;
}

.brand {
  font-weight: bold;
  font-size: 1rem;
  color: #333333;
}

.nav-links {
  display: flex;
  gap: 24px;
}

.nav-links a {
  text-decoration: underline;
  color: #d39bc2;
  font-size: 0.95rem;
}

.nav-links a:hover {
  color: #e4c4d9;
}

/* HERO SECTION */
/* .hero {
  background: linear-gradient(135deg, #c48bba, #db96ca);
  padding: 80px 20px;
  text-align: cente
  color: #ffffff;
}

.hero h1 {
  font-size: 2.4rem;
  font-weight: bold;
  margin-bottom: 16px;
  max-width: 700px;
  margin-left: auto;
  margin-right: auto;
}

.hero p {
  font-size: 1.1rem;
  margin-bottom: 32px;
  opacity: 0.9;
}

.hero-btn {
  display: inline-block;
  padding: 12px 32px;
  background-color: #ffffff;
  color: #ecbedf;
  font-weight: bold;
  font-size: 1rem;
  text-decoration: none;
  border-radius: 999px;
  transition: background-color 0.3s, transform 0.2s;
} */

/* .hero-btn:hover {
  background-color: #ede7ff;
  transform: scale(1.05);
} */

/* FEATURES SECTION */
.features {
  display: flex;
  gap: 24px;
  flex-wrap: wrap;
  justify-content: center;
  padding: 60px 20px;
  background-color: #f9f9f9;
}

.card {
  background: #ffffff;
  border-radius: 14px;
  padding: 32px 24px;
  width: 280px;
  text-align: center;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  border: 1px solid #eeeeee;
  transition: transform 0.2s, box-shadow 0.2s;
}

.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.12);
}

.card-icon {
  font-size: 2.5rem;
  display: block;
  margin-bottom: 14px;
}

.card h3 {
  font-size: 1.15rem;
  font-weight: bold;
  margin-bottom: 8px;
  color: #333333;
}

.card p {
  font-size: 0.95rem;
  color: #666666;
  line-height: 1.5;
}

/* FOOTER */
.footer {
  padding: 20px 32px;
  background-color: #ffffff;
  text-align: left;
}

.footer p {
  font-size: 0.85rem;
  color: #333333;
}
 
 .video {
  padding-bottom: 70px;
  margin-right: 10px;
  margin-left: 10px;
  border-radius: 20px;
  display: flex;
 }
</style>


