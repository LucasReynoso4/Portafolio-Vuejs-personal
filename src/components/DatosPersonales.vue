<script setup>

import instagram from '/src/assets/instagram_icon.svg';
import github from '/src/assets/github_icon.svg';


const title = 'Lucas Reynoso ' ;
const descripcion = 'Estudiante de la UTN Tecnicatura Universitaria en Programación ';
const residencia = 'Longchamps, Buenos Aires, Argentina';
const presentacion = 'Hola, Bienvenido a mi portafolio de proyectos. Soy un estudiante de la Tecnicatura en Programación ¡Gracias por la visita!.';
const redesSociales = [

  { id: 1, name: 'Instagram', src: instagram, url: 'https://www.instagram.com/reynosolucas_/' },
  { id: 2, name: 'github', src: github, url: 'https://github.com/LucasReynoso4' },
  
];
const telefono = '+54 11 6307 9508';
</script>

<template>
  <section class="datos-personales">
    <div class="card">
      <h1>{{ title }}</h1>
      <h2>{{ descripcion }}</h2>
      <p>{{ presentacion }}</p>
      <ul class="container-lista">
        <li v-for="red in redesSociales" :key="red.id">
          <a :href="red.url"><img class="icon-redsocial" :src="red.src" width="35rem" :alt="red.name"></a>
        </li>
      </ul>
      <h3>☎ Mi Teléfono personal: {{ telefono }}</h3>
      <h4>{{ residencia }}</h4>
    </div>
  </section>
</template>

<style scoped>
h1 {
  font-size: 3.5rem;
}

p {
  font-size: 1.2rem;
  font-weight: 600;
  margin-bottom: 1rem;
}

.card {
  background-color: rgb(10, 111, 194);
  border-radius: 10px;
  padding: 30px;
  margin: 30px;
  text-align: center;
}

.container-lista {
  display: flex;
  justify-content: center;
  list-style: none;
  padding: 0;
  margin: 0;
  text-align: center;
}

.icon-redsocial {
  align-items: center;
  background-color: rgb(19, 119, 206);
  border-radius: 50%;
  padding: 2px;
  margin: 5px;
  box-shadow: 0 0 5px rgba(95, 124, 205, 0.934);
}

.icon-redsocial:hover {
  background-color: rgb(28, 41, 52);
  box-shadow: 0 0 5px rgba(251, 249, 249, 0.934);
}

h3 {
  font-size: 1.5rem;
  font-weight: 600;
}
</style>