<template>
  <div>
    <!-- <div class="scroll-up-btn">
      <i class="fas fa-angle-up"></i>
    </div> -->
    <!-- <nav class="nav-area">
      <div class="content">
        <div class="logo">
          <a href="#">Portfo<span>lio.</span></a>
        </div>
        <ul class="navbar">
          <li><router-link to="/">Home</router-link> </li>
          <li><router-link to="/about">About</router-link></li>
          <li><router-link to="/projects">Projects</router-link></li>
          <li><router-link to="/testimonials">Testimonials</router-link></li>
          <li><router-link to="/resume">Resume</router-link></li>
          <li><router-link to="/contact">Contact</router-link></li>
        </ul>
        <div class="menu-btn">
          <i class="fas fa-bars"></i>
        </div>
      </div>
    </nav> -->
    <nav
      class="navbar navbar-expand-lg"
      style="background-color: rgb(222, 191, 181)"
    >
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Portfo<span>lio.</span></a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#"><router-link to="/">Home</router-link></a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href=""><router-link to="/about">About</router-link></a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href=""><router-link to="/projects">Projects</router-link></a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href=""><router-link to="/testimonials">Testimonials</router-link></a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href=""><router-link to="/resume">Resume</router-link></a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href=""><router-link to="/contact">Contact</router-link></a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
</style>
