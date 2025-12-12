<template>
  <div class="sign bgg">
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

    <div class="container-fluid">
      <h5 class="notmember">Not a member?<router-link to="/signup">Sign up now</router-link></h5>

      <!-- SIGN IN -->
      <main class="form-signin w-100 m-auto">
        <form>
          <img class="mb-4" src="/img/logo_small_icon_only.png" alt="" width="60" height="60" />
          <h1 class="h3 mb-3 fw-normal">Please sign in</h1>

          <div class="form-floating">
            <input type="email" class="form-control" id="floatingInput" placeholder="name@example.com" />
            <label for="floatingInput">Email address</label>
          </div>
          <div class="form-floating">
            <input type="password" class="form-control" id="floatingPassword" placeholder="Password" />
            <label for="floatingPassword">Password</label>
          </div>

          <div class="checkbox mb-3">
            <label> <input type="checkbox" value="remember" /> Remember me </label>
          </div>
          <router-link to="/"><button class="w-100 btn btn-lg btn-primary" type="submit">Sign in</button></router-link>
          <p class="mt-2 mb-0 text-muted">&copy; 2022</p>
        </form>
      </main>
      <!-- END -->
    </div>
  </div>
</template>

<script>
export default {
  name: "LoginSign",
  props: {
    msg: String,
  },
};
</script>

<style>
.notmember {
  position: absolute;
  left: 1080px;
  font-size: small;
  top: 80px;
}
body {
  /* display: flex; */
  align-items: center;
  /* padding-top: 40px; */
  padding-bottom: 40px;
  /* background-color: #f5f5f5; */
  background-image: url(https://images.unsplash.com/photo-1492707892479-7bc8d5a4ee93?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=465&q=80);
  background-repeat: no-repeat;
  background-size: 50%;
}

.form-signin {
  position: relative;
  top: 60px;
  left: 300px;
  max-width: 370px;
  padding: 15px;
}

.form-signin .form-floating:focus-within {
  z-index: 2;
}

.form-signin input[type="email"] {
  margin-bottom: -1px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}

.form-signin input[type="password"] {
  margin-bottom: 10px;
  border-top-left-radius: 0;
  border-top-right-radius: 0;
}

.navbar {
  background: #e3e2e7;
}
</style>
