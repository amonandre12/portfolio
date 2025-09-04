<template>
    <footer>
      <div class="footer-container">
        <p>&copy; {{ new Date().getFullYear() }} - AMON | Développeur Front-end React & Vue.js</p>
        <div class="social-links">
          <a href="https://www.linkedin.com/in/blin-wadja-andré-amon-00050a337/" target="_blank" title="LinkedIn">
            <i class="fab fa-linkedin"></i>
          </a>
          <a href="https://github.com/amonandre12" target="_blank" title="GitHub">
            <i class="fab fa-github"></i>
          </a>
        </div>
      </div>
    </footer>
  </template>
  
  <script>
  export default {};
  </script>
  
  <style scoped>
  footer {
    background: #333;
    color: white;
    text-align: center;
    padding: 20px 0;
    margin-top: 50px;
  }
  
  .footer-container {
    display: flex;
    flex-direction: column;
    gap: 10px;
    align-items: center;
    justify-content: center;
  }
  
  .social-links {
    display: flex;
    gap: 20px;
  }
  
  .social-links a {
    color: #00dfc0;
    font-size: 24px;
    transition: color 0.3s ease;
  }
  
  .social-links a:hover {
    color: #00b89c;
  }
  </style>