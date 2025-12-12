<script setup>
import Kategori from "@/assets/Kategori";
</script>

<template>
  <div class="hello">
    <!-- NAVBAR -->
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
            <!-- <li class="nav-item">
              <a class="nav-link text-dark" href="#">SHOP</a>
            </li>
            <li class="nav-item">
              <a class="nav-link text-dark" href="">REVIEW</a>
            </li> -->
            <li class="nav-item">
              <a class="nav-link active text-dark" href=""><router-link to="/">HOME</router-link></a>
            </li>
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
    <!-- END -->
    <!-- HEADER -->
    <div class="container-fluid header">
      <div class="position-relative p-3 p-md-5 text-center prod">
        <div class="col-md-5 p-lg-5 mx-auto my-5">
          <img src="/img/men/kemeja-orang/Garment-Dyed_Oxford_Shirt.png" alt="" class="men" />
          <img src="/img/women/photo1661039990__1_-removebg-preview.png" alt="" class="women" />
          <h1 class="display-2 fw-normal">BALENDA</h1>
          <h6 class="fw-italic">Solution for your outfit of the day</h6>
          <!-- <p class="new-collection">NEW COLLECTION</p> -->
          <!-- <a class="btn btn-outline-secondary" href="#">Coming soon</a> -->
        </div>
        <div class="product-device shadow-sm d-none d-md-block"></div>
        <div class="product-device product-device-2 shadow-sm d-none d-md-block"></div>
      </div>
      <!-- END -->

      <!-- CARD -->
      <section id="kategori">
        <div class="container p-3 p-md-5 text-center prod">
          <h3 style="font-family: poppins">Product Recommendation</h3>
          <div class="row">
            <div class="col-lg-3 col-sm-4 mt-4 carde" v-for="data in Kategori" :key="data">
              <div class="card">
                <router-link to="/about"><img :src="data.image" class="card-img-top gambar" alt="..." /></router-link>
                <div class="text-center">
                  <h5 class="card-text title-name">{{ data.nama }}</h5>

                  <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
      <!-- END -->

      <!-- Op -->
      <section id="product">
        <div class="container p-3 p-md-5 mt-5 text-center prod">
          <h3 style="font-family: poppins">Why You Picking Us</h3>
          <h6>We only provide quality products for customer satisfaction</h6>
          <div class="row">
            <div class="col-lg-3 col-sm-4 mt-5 carde">
              <div class="card border-dark cardd">
                <div class="card-body">
                  <h1 class="text-center">
                    <svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" fill="currentColor" class="bi bi-truck" viewBox="0 0 16 16">
                      <path
                        d="M0 3.5A1.5 1.5 0 0 1 1.5 2h9A1.5 1.5 0 0 1 12 3.5V5h1.02a1.5 1.5 0 0 1 1.17.563l1.481 1.85a1.5 1.5 0 0 1 .329.938V10.5a1.5 1.5 0 0 1-1.5 1.5H14a2 2 0 1 1-4 0H5a2 2 0 1 1-3.998-.085A1.5 1.5 0 0 1 0 10.5v-7zm1.294 7.456A1.999 1.999 0 0 1 4.732 11h5.536a2.01 2.01 0 0 1 .732-.732V3.5a.5.5 0 0 0-.5-.5h-9a.5.5 0 0 0-.5.5v7a.5.5 0 0 0 .294.456zM12 10a2 2 0 0 1 1.732 1h.768a.5.5 0 0 0 .5-.5V8.35a.5.5 0 0 0-.11-.312l-1.48-1.85A.5.5 0 0 0 13.02 6H12v4zm-9 1a1 1 0 1 0 0 2 1 1 0 0 0 0-2zm9 0a1 1 0 1 0 0 2 1 1 0 0 0 0-2z"
                      />
                    </svg>
                  </h1>
                  <h5 class="card-title text-center">Free Shipping</h5>
                  <p class="card-text">The ultimate clothing to see the world in. Be exclusive, Be Devine, Be yourself.</p>
                </div>
              </div>
            </div>
            <div class="col-lg-3 col-sm-4 mt-5 carde">
              <div class="card border-dark cardd">
                <div class="card-body">
                  <h1 class="text-center">
                    <svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" fill="currentColor" class="bi bi-credit-card" viewBox="0 0 16 16">
                      <path d="M0 4a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V4zm2-1a1 1 0 0 0-1 1v1h14V4a1 1 0 0 0-1-1H2zm13 4H1v5a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1V7z" />
                      <path d="M2 10a1 1 0 0 1 1-1h1a1 1 0 0 1 1 1v1a1 1 0 0 1-1 1H3a1 1 0 0 1-1-1v-1z" />
                    </svg>
                  </h1>
                  <h5 class="card-title text-center">Secured Payment</h5>
                  <p class="card-text">Online shopping is very convenient, but cardholders are indeed much more vulnerable online than physical shopping.</p>
                </div>
              </div>
            </div>
            <div class="col-lg-3 col-sm-4 mt-5 carde">
              <div class="card border-dark cardd">
                <div class="card-body">
                  <h1 class="text-center">
                    <svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" fill="currentColor" class="bi bi-gear" viewBox="0 0 16 16">
                      <path d="M8 4.754a3.246 3.246 0 1 0 0 6.492 3.246 3.246 0 0 0 0-6.492zM5.754 8a2.246 2.246 0 1 1 4.492 0 2.246 2.246 0 0 1-4.492 0z" />
                      <path
                        d="M9.796 1.343c-.527-1.79-3.065-1.79-3.592 0l-.094.319a.873.873 0 0 1-1.255.52l-.292-.16c-1.64-.892-3.433.902-2.54 2.541l.159.292a.873.873 0 0 1-.52 1.255l-.319.094c-1.79.527-1.79 3.065 0 3.592l.319.094a.873.873 0 0 1 .52 1.255l-.16.292c-.892 1.64.901 3.434 2.541 2.54l.292-.159a.873.873 0 0 1 1.255.52l.094.319c.527 1.79 3.065 1.79 3.592 0l.094-.319a.873.873 0 0 1 1.255-.52l.292.16c1.64.893 3.434-.902 2.54-2.541l-.159-.292a.873.873 0 0 1 .52-1.255l.319-.094c1.79-.527 1.79-3.065 0-3.592l-.319-.094a.873.873 0 0 1-.52-1.255l.16-.292c.893-1.64-.902-3.433-2.541-2.54l-.292.159a.873.873 0 0 1-1.255-.52l-.094-.319zm-2.633.283c.246-.835 1.428-.835 1.674 0l.094.319a1.873 1.873 0 0 0 2.693 1.115l.291-.16c.764-.415 1.6.42 1.184 1.185l-.159.292a1.873 1.873 0 0 0 1.116 2.692l.318.094c.835.246.835 1.428 0 1.674l-.319.094a1.873 1.873 0 0 0-1.115 2.693l.16.291c.415.764-.42 1.6-1.185 1.184l-.291-.159a1.873 1.873 0 0 0-2.693 1.116l-.094.318c-.246.835-1.428.835-1.674 0l-.094-.319a1.873 1.873 0 0 0-2.692-1.115l-.292.16c-.764.415-1.6-.42-1.184-1.185l.159-.291A1.873 1.873 0 0 0 1.945 8.93l-.319-.094c-.835-.246-.835-1.428 0-1.674l.319-.094A1.873 1.873 0 0 0 3.06 4.377l-.16-.292c-.415-.764.42-1.6 1.185-1.184l.292.159a1.873 1.873 0 0 0 2.692-1.115l.094-.319z"
                      />
                    </svg>
                  </h1>
                  <h5 class="card-title text-center">Support 24/7</h5>
                  <p class="card-text">we are online every day, if you need help we are ready to help</p>
                </div>
              </div>
            </div>
          </div>
          <!-- <button class="rounded bg-a">See More</button> -->
        </div>
      </section>

      <!-- END -->
    </div>
    <!-- EMD -->

    <!-- REVIEW -->

    <!-- END -->

    <!-- FOOTER -->
    <section id="footer">
      <div class="container-fluid footer">
        <footer class="py-5">
          <div class="row">
            <div class="col-7 col-md-3 mb-3">
              <h6>CONTACT US</h6>
              <ul class="nav flex-column">
                <li class="nav-item mb-2"><i>balenda@gmail.com</i></li>
                <li class="nav-item mb-2"><i>+62 9522 98741</i></li>
                <li class="nav-item mb-2"><i>Monday - Saturday: 10:00 am to 5pm (WIB)</i></li>
              </ul>
            </div>
            <div class="col-6 col-md-2 mb-3">
              <h5></h5>
              <ul class="nav flex-column">
                <li class="nav-item mb-2"></li>
                <li class="nav-item mb-2"></li>
                <li class="nav-item mb-2"></li>
                <li class="nav-item mb-2"></li>
                <li class="nav-item mb-2"></li>
              </ul>
            </div>
            <div class="col-6 col-md-2 mb-3">
              <h5></h5>
              <ul class="nav flex-column">
                <li class="nav-item mb-2"></li>
                <li class="nav-item mb-2"></li>
                <li class="nav-item mb-2"></li>
                <li class="nav-item mb-2"></li>
                <li class="nav-item mb-2"></li>
              </ul>
            </div>
            <div class="col-md-4 offset-md-1 mb-3">
              <form>
                <h5>Subscribe to our newsletter</h5>
                <p>Monthly digest of what's new and exciting from us.</p>
                <div class="d-flex flex-column flex-sm-row w-100 gap-2">
                  <label for="newsletter1" class="visually-hidden">Email address</label>
                  <input id="newsletter1" type="text" class="form-control" placeholder="Email address" />
                  <button class="btn btn-primary" type="button">Subscribe</button>
                </div>
              </form>
            </div>
          </div>
          <div>
            <p>&copy; 2022 Balenda, Inc. All rights reserved. Kelompok 22</p>
          </div>
        </footer>
      </div>
    </section>
    <!-- END -->
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },

  data: function () {
    return {
      // kategori: [
      //   {
      //     nama: "WOMEN'S",
      //     image: "https://images.unsplash.com/photo-1427348693976-99e4aca06bb9?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8dmlzaW9ufGVufDB8fDB8fA%3D%3D&w=1000&q=80",
      //   },
      //   {
      //     nama: "ACCESORIES",
      //     image: "https://images.unsplash.com/photo-1427348693976-99e4aca06bb9?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8dmlzaW9ufGVufDB8fDB8fA%3D%3D&w=1000&q=80",
      //   },
      //   {
      //     nama: "MEN'S",
      //     image: "https://images.unsplash.com/photo-1501139083538-0139583c060f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8dGltZXxlbnwwfHwwfHw%3D&w=1000&q=80",
      //   },
      // ],
    };
  },
  // methods: {
  //   changeTitle(data) {
  //     this.titleHero = data.;
  //     this.titleImage = data.image;
  //   },
  // },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.men {
  position: absolute;
  left: 60px;
  width: 300px;
  top: 100px;
}
.women {
  position: absolute;
  right: 40px;
  width: 370px;
  top: 0px;
}
.prod {
  position: relative;
  background-color: #e3e2e7;
  height: 499px;
}
.new-collection {
  position: absolute;
  left: 30px;
  width: 300px;
  top: 50px;
  font-size: 40px;
  float: left;
}
.header {
  background-color: #e3e2e7;
  left: 100px;
}
.footer {
  background-color: white;
  position: relative;
}
.gakpake {
  color: white;
}
.card {
  width: 15rem;
  border-radius: 15px;
  border: 1px;
}
.cardd {
  margin-right: auto;
  margin-left: auto;
  width: 245px;
  box-shadow: 0 15px 25px rgba(129, 124, 124, 0.2);
  height: 300px;
  border-radius: 5px;
  backdrop-filter: blur(14px);
  background-color: rgba(255, 255, 255, 0.2);
  padding: 20px;
  text-align: justify;
}

.carde {
  position: relative;
  left: 150px;
}

.navbar {
  background: #e3e2e7;
}
</style>
