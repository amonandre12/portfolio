<script setup>
defineProps({
  name: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="hero-section">
    <!-- <h1>Salut, je suis <span>{{ name }}</span></h1> -->
    <h2>Développeur Front-End React & Vue.js </h2>
    <p>Je crée des sites modernes et responsives avec <strong>React.js</strong>, <strong>Vue.js</strong>, <strong>TypeScript</strong>, HTML, CSS & javascript</p>

    <a href="/portfolio/CV AMON.pdf" class="btn" download="cv_amon.pdf">Télécharder mon CV</a>
  </div>
</template>

<style scoped>
.hero-section {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: linear-gradient(135deg, #333, #555);
  /* background-color:#0A2BA8 ; */
  color: white;
  text-align: center;
  margin-top: 45px;
  padding-top: 80px;
  
}

.hero-section h1 {
  font-size: 3rem;
  margin-bottom: 10px;
}

.hero-section span {
  color: #00dfc0;
}

.hero-section h2 {
  font-size: 1.8rem;
  margin-bottom: 20px;
}

.hero-section p {
  font-size: 1.2rem;
  margin-bottom: 30px;
}

.btn {
  text-decoration: none;
  padding: 10px 20px;
  background: #00dfc0;
  color: #333;
  border-radius: 5px;
  transition: background 0.3s ease;
}

.btn:hover {
  background: #00b89c;
}
</style>