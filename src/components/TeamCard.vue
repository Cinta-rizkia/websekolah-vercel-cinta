<script setup>
defineProps(['nama', 'jabatan', 'foto'])
</script>

<template>
  <div class="team-card">
    <div class="avatar">
      <img v-if="foto" :src="foto" :alt="nama" />
      <span v-else>{{ nama.charAt(0) }}</span>
    </div>
    <h3 class="nama">{{ nama }}</h3>
    <p class="jabatan">{{ jabatan }}</p>
  </div>
</template>

<style scoped>
.team-card {
  text-align: center;
  padding: 1.5rem 1rem;
  border-radius: 12px;
  background: #fff;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
}

.avatar {
  width: 80px;
  height: 80px;
  margin: 0 auto 1rem;
  border-radius: 50%;
  background: #eccbf3; /* sesuaikan dengan warna tema landing page */
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  font-size: 1.5rem;
  font-weight: bold;
  color: #fff;
}

.avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.nama {
  margin: 0.25rem 0;
  font-size: 1.1rem;
}

.jabatan {
  color: #ebd5ee;
  font-size: 0.9rem;
  margin: 0;
}
</style>