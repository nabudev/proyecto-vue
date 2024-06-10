<template>
    <v-app-bar app color="black" dark flat class="px-12">
      <v-btn >
        NAHUEL-DEV
      </v-btn>
      
  
      <v-spacer></v-spacer>
      <v-btn text @click="scroll('home')" class="text-yellow">Inicio</v-btn>
      <v-btn text @click="scroll('about')"  >Acerca de</v-btn>
      <v-btn text @click="scroll('services')"  >Proyectos</v-btn>
      <v-btn text @click="scroll('contact')"  > Contacto</v-btn>
    </v-app-bar>
  </template>
  
  <script>
  export default {
    methods: {
      scroll(refName) {
        const element = document.getElementById(refName);
        element.scrollIntoView({ behavior: "smooth" });
      },
    },
  };
  </script>
  
  <style>
  
  </style>