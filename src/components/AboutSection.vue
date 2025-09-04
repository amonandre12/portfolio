<script setup>
import MainContent from './MainContent.vue'



// const openReadmeInEditor = () => fetch('/__open-in-editor?file=README.md')
</script>

<template>

<div class="about-content">
  <MainContent>
    <template #heading><span class = "span_style">À propos de moi</span></template>

    <p>
      Mon portfolio reflète ma passion pour le développement front-end.
      J’y présente des interfaces modernes, performantes et centrées sur l’utilisateur, réalisées avec React.js, Vue.js, JavaScript, TypeScript, HTML et CSS.
      Ma rigueur technique et ma créativité me permettent de transformer des maquettes en expériences digitales fluides et intuitives. 
      Découvrez la valeur que je peux apporter à vos projets.
    </p>
   </MainContent>

</div>



</template>

<style scoped>
.about-content {
  padding: 30px 30px ;
  text-align: center;
  background: #f5f5f5;
}

.span_style {
  font-size: 2.5rem;
  margin-bottom: 30px;
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