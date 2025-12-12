<script setup>
import Products from "@/assets/Products";
import Productw from "@/assets/Productw";
import Producta from "@/assets/Producta";
</script>
<template>
  <div class="produk py-5">
    <div class="container">
      <!-- Section Men -->
      <section id="men" class="mb-5">
        <div class="section-header text-center mb-5">
          <h2 class="display-4 fw-bold">MEN'S COLLECTION</h2>
          <div class="divider mx-auto"></div>
        </div>
        
        <div class="row g-4">
          <div class="col-12 col-sm-6 col-lg-3" v-for="data in Products" :key="data">
            <div class="card h-100 product-card">
              <div class="card-img-wrapper">
                <img :src="data.image" class="card-img-top" :alt="data.nama" />
              </div>
              <div class="card-body text-center d-flex flex-column justify-content-between">
                <h5 class="card-title fw-bold mb-2">{{ data.nama }}</h5>
                <p class="card-text text-accent fw-bold">{{ data.harga }}</p>
                <button class="btn btn-outline-dark btn-sm rounded-pill mt-2">View Details</button>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Section Women -->
      <section id="women" class="mb-5">
        <div class="section-header text-center mb-5">
          <h2 class="display-4 fw-bold">WOMEN'S COLLECTION</h2>
          <div class="divider mx-auto"></div>
        </div>

        <div class="row g-4">
          <div class="col-12 col-sm-6 col-lg-3" v-for="data in Productw" :key="data">
             <div class="card h-100 product-card">
              <div class="card-img-wrapper">
                <img :src="data.image" class="card-img-top" :alt="data.nama" />
              </div>
              <div class="card-body text-center d-flex flex-column justify-content-between">
                <h5 class="card-title fw-bold mb-2">{{ data.nama }}</h5>
                <p class="card-text text-accent fw-bold">{{ data.harga }}</p>
                <button class="btn btn-outline-dark btn-sm rounded-pill mt-2">View Details</button>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Section Accessories -->
      <section id="accessories" class="mb-5">
        <div class="section-header text-center mb-5">
          <h2 class="display-4 fw-bold">ACCESSORIES</h2>
          <div class="divider mx-auto"></div>
        </div>

        <div class="row g-4">
           <div class="col-12 col-sm-6 col-lg-3" v-for="data in Producta" :key="data">
             <div class="card h-100 product-card">
              <div class="card-img-wrapper">
                <img :src="data.image" class="card-img-top" :alt="data.nama" />
              </div>
              <div class="card-body text-center d-flex flex-column justify-content-between">
                <h5 class="card-title fw-bold mb-2">{{ data.nama }}</h5>
                <p class="card-text text-accent fw-bold">{{ data.harga }}</p>
                <button class="btn btn-outline-dark btn-sm rounded-pill mt-2">View Details</button>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductJual",
  props: {
    msg: String,
  },
};
</script>

<style scoped>
.produk {
  background-color: var(--background-light);
}

.section-header h2 {
  color: var(--primary-color);
  font-family: var(--font-main);
  letter-spacing: 2px;
}

.divider {
  height: 4px;
  width: 60px;
  background-color: var(--accent-color);
  border-radius: 2px;
}

.product-card {
  border: none;
  background: white;
  transition: all 0.3s ease;
  overflow: hidden;
}

.product-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 30px rgba(0,0,0,0.1);
}

.card-img-wrapper {
  overflow: hidden;
  height: 250px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #f8f9fa;
}

.card-img-top {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
}

.product-card:hover .card-img-top {
  transform: scale(1.1);
}

.card-title {
  font-size: 1.1rem;
  color: var(--secondary-color);
}

.text-accent {
  color: var(--accent-color);
  font-size: 1.2rem;
}

.btn-outline-dark {
  border-color: var(--secondary-color);
  color: var(--secondary-color);
}

.btn-outline-dark:hover {
  background-color: var(--secondary-color);
  color: white;
}
</style>