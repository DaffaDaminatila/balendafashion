<template>
  <div class="login-container">
    <div class="row m-0 h-100">
      <!-- Left Side - Image/Brand -->
      <div class="col-md-6 p-0 d-none d-md-block brand-side">
        <div class="brand-overlay d-flex flex-column justify-content-center align-items-center text-white h-100">
          <h1 class="display-3 fw-bold mb-4">BALENDA</h1>
          <p class="lead">Fashion for the Future</p>
        </div>
      </div>

      <!-- Right Side - Form -->
      <div class="col-md-6 d-flex align-items-center justify-content-center bg-white">
        <div class="form-wrapper p-5 w-100">
          <div class="text-center mb-5">
            <h2 class="fw-bold text-secondary">Welcome Back</h2>
            <p class="text-muted">Please sign in to your account</p>
          </div>

          <form @submit.prevent>
            <div class="form-floating mb-3">
              <input type="email" class="form-control" id="floatingInput" placeholder="name@example.com" />
              <label for="floatingInput">Email address</label>
            </div>
            <div class="form-floating mb-3">
              <input type="password" class="form-control" id="floatingPassword" placeholder="Password" />
              <label for="floatingPassword">Password</label>
            </div>

            <div class="d-flex justify-content-between align-items-center mb-4">
              <div class="form-check">
                <input class="form-check-input" type="checkbox" value="" id="rememberCheck">
                <label class="form-check-label text-muted" for="rememberCheck">
                  Remember me
                </label>
              </div>
              <a href="#" class="text-accent text-decoration-none small">Forgot password?</a>
            </div>

            <button class="w-100 btn btn-lg btn-primary mb-3" type="submit">Sign in</button>
            
            <div class="text-center mt-4">
               <p class="mb-0 text-muted">Not a member? <router-link to="/signup" class="text-accent fw-bold text-decoration-none">Sign up now</router-link></p>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LoginSign",
};
</script>

<style scoped>
.login-container {
  min-height: calc(100vh - 70px); /* Adjust based on navbar height */
  overflow: hidden;
}

.brand-side {
  background-image: url('https://images.unsplash.com/photo-1492707892479-7bc8d5a4ee93?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
  background-size: cover;
  background-position: center;
  position: relative;
}

.brand-overlay {
  background: rgba(44, 54, 57, 0.6); /* Primary color with opacity */
  backdrop-filter: blur(2px);
}

.form-wrapper {
  max-width: 500px;
}

.text-accent {
  color: var(--accent-color);
}

.btn-primary {
  background-color: var(--secondary-color);
  border: none;
}

.btn-primary:hover {
  background-color: var(--accent-color);
}
</style>
