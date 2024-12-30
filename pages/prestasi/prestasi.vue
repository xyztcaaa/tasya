<template>
  <div class="container">
    <h1 class="judul">Prestasi</h1>
    <div class="card-row">
      <div class="card">
        <img src="assets/img/lomba/lomba1.jpg" alt="Lomba 1" class="image">
        <div class="overlay">
          <div class="text">Kunjungan Edukasi Duta Safety Riding</div>
        </div>
      </div>
      <div class="card">
        <img src="assets/img/lomba/lomba2.jpg" alt="Lomba 2" class="image">
        <div class="overlay">
          <div class="text">Juara 2 Bidang Lomba Film Pende & Juara 2 Bidang Lomba Kriya</div>
        </div>
      </div>
      <div class="card">
        <img src="assets/img/lomba/lmba3.jpg" alt="Lomba 3" class="image">
        <div class="overlay">
          <div class="text">Piagam Penghargaan Beasiswa dari Perimajasa PPLG</div>
        </div>
      </div>
      <div class="card">
        <img src="assets/img/lomba/lomba4.jpg" alt="Lomba 4" class="image">
        <div class="overlay">
          <div class="text">Piagam Penghargaan Beasiswa dari Perimajasa DKV</div>
        </div>
      </div>
      <div class="card">
        <img src="assets/img/lomba/lomba5.jpg" alt="Lomba 5" class="image">
        <div class="overlay">
          <div class="text">Piagam Penghargaan Beasiswa dari Perimajasa</div>
        </div>
      </div>
      <div class="card">
        <img src="assets/img/lomba/lomba6.jpg" alt="Lomba 6" class="image">
        <div class="overlay">
          <div class="text">Juara 3
            Atletik (Panca Lomba) Putra O2SN SMK Tingkat Jawa Barat 2024</div>
        </div>
      </div>
    </div>
    <div class="text-center mt-4">
      <NuxtLink to="https://www.instagram.com/smkn4tsmofficial?igsh=YWRkMTNkaW9jNXE4">
        <button class="tombol-btn">Lihat Lainnya</button>
      </NuxtLink>
    </div>
  </div>
  
</template>

<style scoped>
.container {
  text-align: center;
  margin-top: 7rem;
  padding: 20px;
}

.juduul {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 3rem;
  color: #333;
}

.card-row {
  display: flex;
  justify-content: center;
  gap: 30px;
  margin-top: 2rem;
  flex-wrap: wrap;
}

.card {
  position: relative;
  width: 350px;
  height: 220px;
  overflow: hidden;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.card:hover {
  transform: translateY(-10px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

.image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
  border-radius: 12px;
}


.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.6);
  display: flex;
  justify-content: center;
  align-items: center;
  opacity: 0;
  border-radius: 12px;
  transition: opacity 0.3s ease;
}

.card:hover .overlay {
  opacity: 1;
}


.text {
  color: white;
  font-size: 18px;
  text-align: center;
  font-weight: bold;
}

.tombol-btn {
  display: inline-block;
  padding: 12px 24px;
  background-color: #92c7ff;
  color: white;
  font-size: 16px;
  border-radius: 4px;
  border: none;
  cursor: pointer;
  text-align: center;
  transition: all 0.3s ease;
  margin-top: 2rem;
}

.tombol-btn:hover {
  background-color: #a1ceff;
  transform: translateY(-2px);
}

.text-center {
  text-align: center;
  margin-top: 30px;
}
</style>
