<script setup>
import NavBar from './components/base/NavBar.vue'
import Footers from './components/base/Footer.vue'
import HeroSection from './components/section/Heros.vue'
import ProfileSection from './components/section/Profile.vue'
import NewsSection from './components/section/News.vue'
import GalerySection from './components/section/Galery.vue'
import LayananSection from './components/section/Layanan.vue'
</script>

<template>
  <nav class="navbar navbar-dark bg-dark sticky-top navbar-expand-lg shadow-sm">
    <NavBar />
  </nav>

  <div id="heros">
    <HeroSection />
  </div>

  <div id="profile">
    <ProfileSection />
  </div>

  <div id="news">
    <NewsSection />
  </div>

  <div id="galery">
    <GalerySection />
  </div>

  <div id="layanan">
    <LayananSection />
  </div>

  <footer class="bg-dark text-center text-lg-start text-white">
    <Footers />
  </footer>
</template>