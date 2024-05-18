<template>
    
    <q-layout view="hHh lpR fFf"> 
        <q-header elevated class="bg-brown text-white" id="header">
        <navbar />
      </q-header>
      
  
      <q-page-container class="content">
        <div class="carousel-container">
          <Carousel/>
        </div>
  
        <div class="card-container">
          <card/>
        </div> 
      </q-page-container>


  <div>
    <q-footer elevated class="bg-brown-8 text-white" id="footer">
        <q-toolbar>
          <q-toolbar-title>
            <div>
              <h5 href="#"> About Us</h5>
              <copyright />
            </div>
          </q-toolbar-title>
        </q-toolbar>
      </q-footer>
    </div>
      
    </q-layout>
    
  </template>
  
  <script setup>
  import navbar from "./navbar.vue"
  import Carousel from "./Carousel.vue"
  import card from "./Cards.vue"
  import copyright from "./copyrights.vue"
  </script>
  
  <style scoped>
  html, body, #q-app {
    height: 100%;
  }
  
  .q-layout {
    display: flex;
    flex-direction: column;
    min-height: 100%; /* Ensure layout stretches to fill the viewport */
  }
  
  .q-page-container {
    flex: 1;
    display: flex;
    flex-direction: column;
  }
  
  .content {
    flex: 1;
    overflow-y: auto;
    padding: 20px; /* Add padding for content */
  }
  
  .carousel-container,
  .card-container {
    margin-bottom: 20px; /* Add margin between carousel and cards */
  }
  
  #header {
    background-color: #795548;
    padding: 20px;
    position: absolute;
    margin:0%;
  }
  
  #footer {
    text-align: center;
    background-color: black;
    padding: 20px 0; /* Adjust padding for footer */
    position:absolute;
  }
  
  h5 {
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    font-size: 100%;
    cursor: pointer;
  }
  </style>
  