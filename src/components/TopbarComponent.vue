<template>
    <nav class="topbar">
      <div class="container">
        <a href="#" class="logo">Logo</a>
        <ul class="menu">
          <li><a href="#about">Sobre</a></li>
          <li><a href="#partners">Parceiros</a></li>
          <li><a href="#footer">Contato</a></li>
        </ul>
      </div>
    </nav>
  </template>
  
  <style scoped>
  .topbar {
    background-color: #06283f;
  }
  
  .container {
    background-color: #06283f;
    width: 100%;
    margin: 0 auto;
    position: fixed;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .logo {
    color: #ffffff;
    font-size: 24px;
    text-decoration: none;
  }
  
  .menu {
    list-style: none;
    margin: 0;
    padding: 0;
  }
  
  .menu li {
    display: inline-block;
    margin-left: 20px;
  }
  
  .menu li:first-child {
    margin-left: 0;
  }
  
  .menu li a {
    color: #ffffff;
    text-decoration: none;
    font-size: 18px;
  }
  </style>
  