<template>
    <section id="projects">
      <div class="projects-container">
        <h2>Mes Projets</h2>
        <div class="projects-grid">
          <div v-for="(project, index) in projects" :key="index" class="project-card">
            <img :src="project.image" :alt="project.title" />
            <div class="project-info">
              <h3>{{ project.title }}</h3>
              <p>{{ project.description }}</p>
              <a :href="project.link" target="_blank" class="btn">Voir le projet</a>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>

  <script>
  export default {
    data() {
      return {
        projects: [
          {
            title: "Jeu de Serpent",
            description: "Jeu interactif avec Vue.js",
            image: "/portfolio/serpent.jpg" ,
            link: "https://amonandre12.github.io/SNAKE-VUE/",
          },
          {
            title: "Site W3.CSS-Template",
            description: "Site responsive pour aliments réaliser avec Vue.js",
            image: "/portfolio/sandwich.jpg" ,
            link: "https://amonandre12.github.io/SITE-FOOD/",
          },

          {
            title: "Un projet de Académie France  ",
            description: "Un projet de Académie France réalisé avec HTML et CSS ",
            image: "/portfolio/images.png" ,
            link: " https://amonandre12.github.io/Academy_site/",
          },


          {
            title: "AzerType",
            description: "Application de saisie rapide",
            image: "/portfolio/form.jpg" ,
            link: "https://amonandre12.github.io/AZERTYPE/",
          },

          {
            title: "Formulaire de conexion",
            description: "Formulaire statique réalisé avec HTML et CSS ",
            image: "/portfolio/lyft.jpg" ,
            link: "https://amonandre12.github.io/FORM-TEST/",
         },
         {
           title: "Site responsive pour designer ",
            description: "Un site web pour presenter ses differents services réalisé avec HTML , CSS et JavaScript",
            image: "/portfolio/home.jpg" ,
            link: "https://amonandre12.github.io/Designer/",
         },
         {
            title: "Formulaire de conexion",
            description: "Formulaire avec validation en temps réel réalisé avec Vue.js",
            image: "/portfolio/logo.jpg" ,
            link: "https://amonandre12.github.io/validation/",
         },
         {
           title: "Site vitrine ",
            description: "Un site pour la presentation des aliments réalisé avec React.js",
            image: "/portfolio/sandwich.jpg" ,
            link: "https://amonandre12.github.io/react_food/",
         },
           {
           title: "Formulaire d'inscription ",
            description: "Un formulaire de contact réalisé avec React.js",
            image: "/portfolio/form.png" ,
            link: " https://amonandre12.github.io/formulaire/",
         },
        ],
      };
    }
  };
  </script>

  <style scoped>
  .projects-container {
    padding: 80px 30px;
    text-align: center;
  }

  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 20px;
  }
  h2 {
    margin-bottom: 30px;
  }
  .project-card {
    background: #f5f5f5;
    border-radius: 10px;
    overflow: hidden;
    transition: transform 0.3s ease;
  }

  .project-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }

  .project-card:hover {
    transform: scale(1.05);
  }

  .project-info {
    padding: 20px;
  }

  .project-info h3 {
    margin-bottom: 10px;
  }

  .btn {
    display: inline-block;
    padding: 10px 20px;
    background: #00dfc0;
    text-decoration: none;
    color: #333;
    border-radius: 5px;
    transition: background 0.3s ease;
  }

  .btn:hover {
    background: #00b89c;
  }
  </style>
