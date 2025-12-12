<script setup>
import Kategori from "@/assets/Kategori";
</script>

<template>
  <div class="landing-page">
    
    <!-- HEADER / HERO -->
    <header class="hero-section text-center position-relative overflow-hidden">
      <div class="container py-5">
        <div class="row align-items-center justify-content-center py-5">
          <!-- Left Image (Desktop) -->
          <div class="col-lg-3 d-none d-lg-block">
            <img src="/img/men/kemeja-orang/Garment-Dyed_Oxford_Shirt.png" alt="Men's Fashion" class="img-fluid hero-img float-animation" />
          </div>

          <!-- Center Text -->
          <div class="col-lg-6 my-5 position-relative z-10">
            <h1 class="display-1 fw-bold hero-title px-4 mb-3">BALENDA</h1>
            <p class="lead fw-normal mb-4 text-muted fst-italic">"Solution for your outfit of the day"</p>
            <div class="d-grid gap-2 d-sm-flex justify-content-sm-center">
              <router-link to="/about" class="btn btn-primary btn-lg px-4 gap-3">Shop Now</router-link>
              <router-link to="/login" class="btn btn-outline-secondary btn-lg px-4">Sign Up</router-link>
            </div>
          </div>

           <!-- Right Image (Desktop) -->
          <div class="col-lg-3 d-none d-lg-block">
             <img src="/img/women/photo1661039990__1_-removebg-preview.png" alt="Women's Fashion" class="img-fluid hero-img float-animation-delayed" />
          </div>
        </div>
        
        <!-- Background decorative elements -->
        <div class="product-device shadow-sm d-none d-md-block"></div>
        <div class="product-device product-device-2 shadow-sm d-none d-md-block"></div>
      </div>
    </header>

    <!-- PRODUCT RECOMMENDATION -->
    <section id="kategori" class="py-5 bg-white">
      <div class="container text-center">
        <div class="section-header mb-5">
           <h2 class="display-5 fw-bold">Product Recommendation</h2>
           <p class="text-muted">Find your perfect style</p>
        </div>
       
        <div class="row justify-content-center">
          <div class="col-md-4 col-sm-6 mb-4" v-for="data in Kategori" :key="data">
            <div class="card h-100 category-card">
              <div class="card-img-top-wrapper">
                 <router-link to="/about">
                   <img :src="data.image" class="card-img-top" :alt="data.nama" />
                 </router-link>
              </div>
              <div class="card-body">
                <h5 class="card-title fw-bold">{{ data.nama }}</h5>
                <router-link to="/about" class="btn btn-sm btn-outline-dark mt-2">Explore</router-link>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- FEATURES -->
    <section id="features" class="py-5 bg-light">
      <div class="container text-center">
        <div class="section-header mb-5">
          <h2 class="display-5 fw-bold">Why Choose Us</h2>
          <p class="text-muted">Quality products for customer satisfaction</p>
        </div>

        <div class="row g-4">
          <!-- Feature 1 -->
          <div class="col-md-4">
            <div class="feature-card p-4 h-100 bg-white rounded-3 shadow-sm">
              <div class="feature-icon mb-3 text-secondary">
                 <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" fill="currentColor" class="bi bi-truck" viewBox="0 0 16 16">
                    <path d="M0 3.5A1.5 1.5 0 0 1 1.5 2h9A1.5 1.5 0 0 1 12 3.5V5h1.02a1.5 1.5 0 0 1 1.17.563l1.481 1.85a1.5 1.5 0 0 1 .329.938V10.5a1.5 1.5 0 0 1-1.5 1.5H14a2 2 0 1 1-4 0H5a2 2 0 1 1-3.998-.085A1.5 1.5 0 0 1 0 10.5v-7zm1.294 7.456A1.999 1.999 0 0 1 4.732 11h5.536a2.01 2.01 0 0 1 .732-.732V3.5a.5.5 0 0 0-.5-.5h-9a.5.5 0 0 0-.5.5v7a.5.5 0 0 0 .294.456zM12 10a2 2 0 0 1 1.732 1h.768a.5.5 0 0 0 .5-.5V8.35a.5.5 0 0 0-.11-.312l-1.48-1.85A.5.5 0 0 0 13.02 6H12v4zm-9 1a1 1 0 1 0 0 2 1 1 0 0 0 0-2zm9 0a1 1 0 1 0 0 2 1 1 0 0 0 0-2z"/>
                  </svg>
              </div>
              <h4 class="fw-bold mb-3">Free Shipping</h4>
              <p class="text-muted">The ultimate clothing to see the world in. Be exclusive, Be Divine, Be yourself.</p>
            </div>
          </div>

           <!-- Feature 2 -->
          <div class="col-md-4">
            <div class="feature-card p-4 h-100 bg-white rounded-3 shadow-sm">
               <div class="feature-icon mb-3 text-secondary">
                  <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" fill="currentColor" class="bi bi-credit-card" viewBox="0 0 16 16">
                    <path d="M0 4a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V4zm2-1a1 1 0 0 0-1 1v1h14V4a1 1 0 0 0-1-1H2zm13 4H1v5a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1V7z" />
                    <path d="M2 10a1 1 0 0 1 1-1h1a1 1 0 0 1 1 1v1a1 1 0 0 1-1 1H3a1 1 0 0 1-1-1v-1z" />
                  </svg>
              </div>
              <h4 class="fw-bold mb-3">Secured Payment</h4>
              <p class="text-muted">Online shopping is very convenient, but cardholders are indeed much more vulnerable.</p>
            </div>
          </div>

           <!-- Feature 3 -->
          <div class="col-md-4">
            <div class="feature-card p-4 h-100 bg-white rounded-3 shadow-sm">
               <div class="feature-icon mb-3 text-secondary">
                  <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" fill="currentColor" class="bi bi-gear" viewBox="0 0 16 16">
                    <path d="M8 4.754a3.246 3.246 0 1 0 0 6.492 3.246 3.246 0 0 0 0-6.492zM5.754 8a2.246 2.246 0 1 1 4.492 0 2.246 2.246 0 0 1-4.492 0z" />
                    <path d="M9.796 1.343c-.527-1.79-3.065-1.79-3.592 0l-.094.319a.873.873 0 0 1-1.255.52l-.292-.16c-1.64-.892-3.433.902-2.54 2.541l.159.292a.873.873 0 0 1-.52 1.255l-.319.094c-1.79.527-1.79 3.065 0 3.592l.319.094a.873.873 0 0 1 .52 1.255l-.16.292c-.892 1.64.901 3.434 2.541 2.54l.292-.159a.873.873 0 0 1 1.255.52l.094.319c.527 1.79 3.065 1.79 3.592 0l.094-.319a.873.873 0 0 1 1.255-.52l.292.16c1.64.893 3.434-.902 2.54-2.541l-.159-.292a.873.873 0 0 1 .52-1.255l.319-.094c1.79-.527 1.79-3.065 0-3.592l-.319-.094a.873.873 0 0 1-.52-1.255l.16-.292c.893-1.64-.902-3.433-2.541-2.54l-.292.159a.873.873 0 0 1-1.255-.52l-.094-.319zm-2.633.283c.246-.835 1.428-.835 1.674 0l.094.319a1.873 1.873 0 0 0 2.693 1.115l.291-.16c.764-.415 1.6.42 1.184 1.185l-.159.292a1.873 1.873 0 0 0 1.116 2.692l.318.094c.835.246.835 1.428 0 1.674l-.319.094a1.873 1.873 0 0 0-1.115 2.693l.16.291c.415.764-.42 1.6-1.185 1.184l-.291-.159a1.873 1.873 0 0 0-2.693 1.116l-.094.318c-.246.835-1.428.835-1.674 0l-.094-.319a1.873 1.873 0 0 0-2.692-1.115l-.292.16c-.764.415-1.6-.42-1.184-1.185l.159-.291A1.873 1.873 0 0 0 1.945 8.93l-.319-.094c-.835-.246-.835-1.428 0-1.674l.319-.094A1.873 1.873 0 0 0 3.06 4.377l-.16-.292c-.415-.764.42-1.6 1.185-1.184l.292.159a1.873 1.873 0 0 0 2.692-1.115l.094-.319z" />
                  </svg>
              </div>
              <h4 class="fw-bold mb-3">Support 24/7</h4>
              <p class="text-muted">We are online every day, if you need help we are ready to help.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  }
};
</script>

<style scoped>
.hero-section {
  background-color: #dcd7c9; /* Light elegant accent */
  background: linear-gradient(135deg, #e3e2e7 0%, #f5f5f5 100%);
  min-height: 80vh;
  display: flex;
  align-items: center;
}

.hero-title {
  color: var(--primary-color);
  letter-spacing: 5px;
}

.hero-img {
  max-height: 400px;
  object-fit: contain;
  filter: drop-shadow(0 10px 10px rgba(0,0,0,0.1));
}

.float-animation {
  animation: float 6s ease-in-out infinite;
}

.float-animation-delayed {
  animation: float 6s ease-in-out infinite 3s;
}

@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
  100% { transform: translateY(0px); }
}

.category-card {
  transition: transform 0.3s;
  border: none;
  overflow: hidden;
}

.category-card:hover {
  transform: translateY(-5px);
}

.card-img-top-wrapper {
  height: 250px;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #f8f9fa;
}

.card-img-top {
  height: 100%;
  width: 100%;
  object-fit: cover;
  transition: transform 0.5s;
}

.category-card:hover .card-img-top {
  transform: scale(1.1);
}

.feature-card {
  transition: all 0.3s;
}

.feature-card:hover {
  transform: translateY(-5px);
  box-shadow: var(--shadow-lg) !important;
}

.feature-icon svg {
  color: var(--secondary-color);
}
</style>
