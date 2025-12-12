<template>
  <footer class="footer mt-auto py-3">
    <div class="container text-center">
      <span class="text-muted">© 2022 Final Project Vue. All rights reserved.</span>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped>
.footer {
  background-color: var(--primary-color);
  color: var(--background-light) !important;
  margin-top: auto;
}
.text-muted {
  color: rgba(255,255,255,0.6) !important;
}
</style>
