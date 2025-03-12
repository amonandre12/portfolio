<script setup>
// import MenuCard from './components/MenuCard.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import ProjectSection from './components/ProjectSection.vue'
import ContactSection from './components/ContactSection.vue'
import FooterSection from './components/FooterSection.vue'

import { ref } from 'vue';
const isMenuOpen = ref(false);
const toggleMenu = () => { isMenuOpen.value = !isMenuOpen.value; };
const closeMenu = () => { isMenuOpen.value = false; };
</script>

<template>
  <header class="header">
    <nav class="nav">
     <a href="#" class="logo"><img src="@/assets/logo.jpg" alt="logo-site"> </a>
      
      <button class="burger" @click="toggleMenu">
        <span></span><span></span><span></span>
      </button>
      <ul :class="{'nav-links': true, 'open': isMenuOpen}">
        <li><a href="#accueil" @click="closeMenu">Accueil</a></li>
        <li><a href="#accueil" @click="closeMenu">À propos</a></li>
        <li><a href="#projets" @click="closeMenu">Projets</a></li>
        <li><a href="#contact" @click="closeMenu">Contact</a></li> 
      </ul>
    </nav>
  </header>

  <main>
    <HeroSection name="AMON" />
    <AboutSection/>
    <ProjectSection/>
    <ContactSection/>
    <FooterSection/>
  </main>
</template>


<style scoped>

.header {
  width: 100%;
  box-shadow: 0 4px 6px rgba(7, 3, 3, 0.1);
  background-color: #fff;
  color: black;
  padding: 1rem;
  position:fixed;
  top:0px;
  z-index:1000;
}
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: auto;
}

 .logo img {
  margin-left: 10px;
  width:100%;
  border-radius: 50%;
  height: 50px;
  cursor: pointer;
}
.burger {
  display: none;
  flex-direction: column;
  cursor: pointer;
  background: none;
  border: none;
}
.burger span {
  width: 25px;
  height: 3px;
  background: black;
  margin: 4px 0;
}
.logo img:hover {
  transform: scale(1.1);
  transition: transform 0.3s ease-in-out;
}
.nav-links {
  list-style: none;
  display: flex;
  gap: 3rem;
}
.nav-links a {
  text-decoration: none;
  color: black;
  cursor:pointer;
  font-size: 18px;
  transition: color 0.3s;
}

.nav-links a:hover {
  color: #00bcd4;
}
@media (max-width: 768px) {
  .burger {
    display: flex;
  }
  .nav-links {
    position: absolute;
    top: 60px;
    right: 0;
    box-shadow: 0 4px 6px rgba(7, 3, 3, 0.1);
    background-color: #fff;
    color: black;
    width: 200px;
    flex-direction: column;
    padding: 1rem;
    display: none;
  }
  .nav-links.open {
    display: flex;
  }
}
</style>