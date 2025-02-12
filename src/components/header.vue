<template>
    <header>
      <h1>DUBOIS Céline</h1>
      <nav>
        <ul>
          <li><a href="#je-suis">Qui Suis-je ?</a></li>
          <li><a href="#projets">Mes Projets</a></li>
          <li><a href="#competences">Mes compétences</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </header>
  </template>
  
  <script>
  export default {
    name: 'Header'
  }
  </script>
  
  <style scoped>
  header {
    background-color: #333;
    color: white;
    padding: 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  nav ul {
    list-style: none;
    display: flex;
    gap: 15px;
  }
  
  nav a {
    color: white;
    text-decoration: none;
  }
  
  nav a:hover {
    text-decoration: underline;
  }
