<template>
  <nav class="navbar">
    <div class="nav-container">
      <router-link to="/" class="nav-brand">
        <img src="../assets/images/specksnyder_logo_v2.jpg" alt="Specksnyder Labs" class="nav-logo">
      </router-link>
      <div class="nav-links">
        <!-- <router-link to="/" class="nav-link">Home</router-link> -->
        <!-- <router-link to="/about" class="nav-link">About</router-link> -->
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'NavBar'
}
</script>

<style scoped>
.navbar {
  background-color: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(10px);
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  padding: 1rem 0;
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
}

.nav-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav-brand {
  text-decoration: none;
  display: flex;
  align-items: center;
}

.nav-logo {
  height: 40px;
  width: auto;
  object-fit: contain;
  transition: opacity 0.3s ease;
}

.nav-logo:hover {
  opacity: 0.8;
}

.nav-links {
  display: flex;
  gap: 2rem;
}

.nav-link {
  text-decoration: none;
  color: #666;
  font-weight: 500;
  transition: color 0.3s ease;
}

.nav-link:hover,
.nav-link.router-link-active {
  color: #333;
}
</style>