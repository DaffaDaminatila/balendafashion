<script setup>
import Products from "@/assets/Products";
import Productw from "@/assets/Productw";
import Producta from "@/assets/Producta";
</script>
<template>
  <div class="produk">
    <nav class="navbar navbar-expand-lg navbar-dark">
      <div class="container">
        <a class="navbar-brand" href="">
          <img src="/img/logo_small.png" alt="" width="140" height="35" />
        </a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarTogglerDemo02" aria-controls="navbarTogglerDemo02" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item">
              <a class="nav-link active text-dark" href=""><router-link to="/">HOME</router-link></a>
            </li>
            <!-- <li class="nav-item">
              <a class="nav-link text-dark" href="#">SHOP</a>
            </li> -->
            <!-- <li class="nav-item">
              <a class="nav-link text-dark" href="">REVIEW</a>
            </li> -->
            <li class="nav-item">
              <a class="nav-link text-dark" href=""><router-link to="/about">PRODUCT</router-link></a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-dark" href=""><router-link to="/login">LOGIN</router-link></a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <section id="product">
      <div class="p-3 p-md-5 text-center prod">
        <div class="row">
          <h3 class="judul">MEN</h3>
          <div class="col mt-4" v-for="data in Products" :key="data">
            <div class="card" style="width: 15rem">
              <img :src="data.image" class="card-img-top" alt="..." />
              <div class="card-body text-center">
                <h5 class="card-title title-name">{{ data.nama }}</h5>
                <h5 class="card-title title-name">{{ data.harga }}</h5>
                <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="p-3 p-md-5 text-center prods">
        <div class="row">
          <h3 class="judul">WOMEN</h3>
          <div class="col mt-4" v-for="data in Productw" :key="data">
            <div class="card" style="width: 15rem">
              <img :src="data.image" class="card-img-top" alt="..." />
              <div class="card-body text-center">
                <h5 class="card-title title-name">{{ data.nama }}</h5>
                <h5 class="card-title title-name">{{ data.harga }}</h5>
                <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="p-3 p-md-5 text-center prode">
        <div class="row">
          <h3 class="judul">ACCESORIES</h3>
          <div class="col mt-4" v-for="data in Producta" :key="data">
            <div class="card" style="width: 15rem">
              <img :src="data.image" class="card-img-top" alt="..." />
              <div class="card-body text-center">
                <h5 class="card-title title-name">{{ data.nama }}</h5>
                <h5 class="card-title title-name">{{ data.harga }}</h5>
                <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
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
.title-name {
  font-size: medium;
  font-family: poppins;
}

html {
  scroll-behavior: smooth;
}

.prod {
  background-color: #3f4e4f;
}
.prods {
  background-color: #a27b5c;
}
.prode {
  background-color: #2c3639;
}
.judul {
  color: white;
}
.navbar {
  background: #e3e2e7;
}
</style>