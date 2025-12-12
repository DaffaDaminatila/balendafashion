<template>
  <nav class="navbar navbar-expand-lg">
    <div class="container">
      <router-link class="navbar-brand" to="/">
        <img src="/img/logo_small.png" alt="Logo" width="140" height="35" class="d-inline-block align-text-top">
      </router-link>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#mainNavbar" aria-controls="mainNavbar" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="mainNavbar">
        <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <router-link class="nav-link" to="/">HOME</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/about">PRODUCT</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link btn-login ms-lg-3" to="/login">LOGIN</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'AppNavbar'
}
</script>

<style scoped>
.navbar {
  background-color: rgba(227, 226, 231, 0.95);
  backdrop-filter: blur(10px);
  box-shadow: 0 2px 10px rgba(0,0,0,0.05);
  position: sticky;
  top: 0;
  z-index: 1000;
  padding: 1rem 0;
}

.nav-link {
  font-weight: 600;
  color: var(--primary-color) !important;
  margin: 0 10px;
  position: relative;
}

.nav-link::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  background: var(--accent-color);
  bottom: 0;
  left: 0;
  transition: width 0.3s;
}

.nav-link:hover::after,
.router-link-active::after {
  width: 100%;
}

.btn-login {
  background-color: var(--secondary-color);
  color: white !important;
  padding: 8px 20px !important;
  border-radius: 20px;
  transition: all 0.3s;
}

.btn-login:hover {
  background-color: var(--accent-color);
  transform: translateY(-2px);
}
.btn-login::after {
  display: none;
}
</style>
