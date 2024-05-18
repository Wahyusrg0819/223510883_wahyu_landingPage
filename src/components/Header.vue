<template>
    <q-layout view="hHh lpR fFf"> 
      <q-header elevated class="bg-brown text-white" id="header">
        <navbar />
      </q-header>
  
      <q-page-container class="content">
        <div>
          <Carousel/>
        </div>
  
        <div>
          <card/>
        </div> 
      </q-page-container>
  
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
    height: 100%;
  }
  
  .q-page-container {
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  
  .content {
    flex: 1;
    overflow-y: auto;
  }
  
  #header {
    background-color: #795548;
    padding: 20px;
    position: relative;
    margin-bottom: -8%;
  }
  
  #footer {
    margin-top: -10%;
    text-align: center;
    background-color: black;
    padding: 0px;
    width: 100%;
    position: relative;
    padding-bottom: 30px;
  }

  h5 {
    font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    font-size:100%;
    cursor: pointer;
  }
  </style>
  