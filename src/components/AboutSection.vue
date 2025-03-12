<script setup>
import MainContent from './MainContent.vue'
import {ref} from 'vue'
const name = ref('AMON')

// const openReadmeInEditor = () => fetch('/__open-in-editor?file=README.md')
</script>

<template>

<div class="about-content">
  <MainContent>
    <template #heading><span>À propos de moi</span></template>

    <p>Je suis <strong>{{ name }} </strong> , développeur web front-end autodidacte passionné  <br/>
      par la création d'interface modernes avec <strong>Vue.js</strong>,HTML,CSS et Javascript.<br/>
      Mon objectif est de transformer des idées en sites web clairs, interactif et 100% responsives.
    </p>
    
  </MainContent>
<p>
  Je crois que chaque projet est une opportunité  d'apprentissage.<br/>
  Même si je suis au debut de ma carrière, ma motivation et ma capacité à trouver des solutions <br/>
  me permettent d'aller toujours de plus loin.
</p>

  <MainContent>
    <p>
      Je suis prêt à collaborer avec des entreprises,<br/> 
      startups ou particuliers pour donner vie à leur projet numérique.
    </p>

    <!-- <a href="#projects" class="btn">Découvrez mes projets</a> -->
  </MainContent>

</div>
</template>

<style scoped>
.about-content {
  padding: 30px 30px ;
  text-align: center;
  background: #f5f5f5;
}

.about-content span {
  font-size: 2.5rem;
  margin-bottom: 20px;
  color: #333;
}

.about-content p  {
font-size: 1.2rem;
margin-bottom: 20px;
color: #555;
}

.about-content .btn {
  display: inline-block;
  padding: 10px 20px;
  background: #00dfc0;
  color: #333;
  text-decoration: none;
  border-radius: 5px;
  transition: background 0.3s ease;
}

.about-content .btn:hover {
  background: #00b89c;
}
</style>