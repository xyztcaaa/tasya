<template>
  <h2 class="title">Seragam Sekolah SMKN 4 Tasikmalaya</h2>
  <div class="grid-container">
    <div v-for="(dkv, i) in seragam" :key="i" class="card">
      <img :src="dkv.foto" alt="senin" class="image">
      <div class="overlay">{{ dkv.judul }}</div>
    </div>
    <!-- <div v-for="(or, i) in seragam" :key="i"  class="card">
      <img :src="or.foto"  alt="rabu" class="image">
      <div class="overlay">{{ or.judul }}</div>
    </div> -->
    <!-- <div class="card">
      <img src="assets/img/baju/pplg.jpeg" alt="pplg" class="image">
      <div class="overlay">Seragam Praktik PPLG</div>
    </div>
    <div class="card">
      <img src="assets/img/baju/dkv.jpeg" alt="dkv" class="image">
      <div class="overlay">Seragam Praktik DKV</div>
    </div>
    <div class="card">
      <img src="assets/img/baju/toi.jpeg" alt="toi" class="image">
      <div class="overlay">Seragam Praktik TOI</div>
    </div>
    <div class="card">
      <img src="assets/img/baju/tjkt.jpeg" alt="tjkt" class="image">
      <div class="overlay">Seragam Praktik TJKT</div>
    </div>
    <div class="card">
      <img src="assets/img/baju/tbsm.jpeg" alt="tbsm" class="image">
      <div class="overlay">Seragam Praktik TBSM</div>
    </div>
    <div class="card">
      <img src="assets/img/baju/jumat.jpeg" alt="jumat" class="image">
      <div class="overlay">Semua Siswa-Siswi</div>
    </div>
    <div class="card">
      <img src="assets/img/baju/or.jpeg" alt="or" class="image">
      <div class="overlay">Semua Siswa-Siswi</div>
    </div>  -->
  </div>
  
</template>

<script setup>
const supabase = useSupabaseClient();

const seragam = ref([]);

const getseragam = async () => {
  const { data, error } = await supabase
    .from("seragam")
    .select(`*`)
   
  if (data) seragam.value = data;
}

onMounted(() => {
  getseragam();

});

</script>

<style scoped>
.title {
  text-align: center;
  font-size: 2rem;
  font-weight: bold;
  color: #333;
  margin-bottom: 2rem;
  margin-top: 8rem;
}

.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr); 
  grid-column-gap: 0.2px; 
  grid-row-gap: 8px; 
  justify-items: center;
  margin: 0 auto;
  padding: 0 1rem;
}

.card {
  position: relative;
  width: 100%;
  max-width: 300px; 
  border-radius: 8px;
  overflow: hidden;
  background: #fff; 
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); 
  margin-top: 0.5rem;
  transition: transform 0.3s ease;
}

.image {
  display: block;
  width: 100%;
  height: auto;
  border-radius: 8px;
  transition: transform 0.3s ease;
}

.overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: rgba(0, 0, 0, 0.6); /* Transparent black background */
  color: white;
  width: 100%;
  padding: 15px;
  text-align: center;
  font-size: 18px;
  opacity: 0;
  transform: translateY(100%);
  transition: opacity 0.5s ease, transform 0.3s ease;
}

.card:hover .overlay {
  opacity: 1;
  transform: translateY(0);
}

/* Zoom */
.card:hover .image {
  transform: scale(1.1); 
}

.card:hover {
  transform: translateY(-5px); 
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2); 
}
</style>
