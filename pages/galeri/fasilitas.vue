<template>
  <div class="container">
    <h2 class="title">Fasilitas Sekolah</h2>
    <div class="card">
      <img src="assets/img/tempat/kantin.jpeg" alt="kantin" class="image">
      <div class="overlay">
        <div class="text">Kantin</div>
      </div>
    </div>
    <div class="card">
      <img src="assets/img/tempat/lpang.jpeg" alt="lpang" class="image">
      <div class="overlay">
        <div class="text">Lapangan</div>
      </div>
    </div>
    <div class="card">
      <img src="assets/img/tempat/mesjid.jpeg" alt="mesjid" class="image">
      <div class="overlay">
        <div class="text">Mesjid</div>
      </div>
    </div>
    <div class="card">
      <img src="assets/img/tempat/perpus.jpeg" alt="perpus" class="image">
      <div class="overlay">
        <div class="text">Perpustakaan</div>
      </div>
    </div>
    <div class="card">
      <img src="assets/img/tempat/seni1.jpeg" alt="seni" class="image">
      <div class="overlay">
        <div class="text">Ruang Seni</div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
  margin-top: 2rem;
}

.title {
  text-align: center;
  font-size: 2rem; /* Ukuran font besar untuk judul */
  font-weight: bold;
  color: #333;
  width: 100%;
  margin-bottom: 2rem; /* Memberikan jarak antara judul dan konten */
  margin-top: 7rem;
}

.card {
  position: relative;
  width: 300px; /* Ukuran card */
  height: 200px;
  overflow: hidden;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
}

.image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 12px;
}

.overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(0, 0, 0, 0.6); /* Background transparan */
  overflow: hidden;
  width: 100%;
  height: 0;
  transition: height 0.5s ease;
  border-radius: 12px;
}

.card:hover .overlay {
  height: 100%;
}

.text {
  color: white;
  font-size: 18px;
  font-weight: bold;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
}
</style>
