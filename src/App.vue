<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>

<header>
      <nav>
        <ul>
          <li><RouterLink to="/">Home</RouterLink></li>
          <li> <RouterLink to="/register">Registrar</RouterLink></li>
          <li> <RouterLink to="/agregar">Agregar</RouterLink></li>
          <li><RouterLink to="/actualizar">Actualizar Clientes</RouterLink></li>
          <li> <RouterLink to="/agregarusuario">Agregar Usuario</RouterLink></li>
          <li><RouterLink to="/actualizarusuario">Actualizar Usuario</RouterLink></li>
        </ul>
      </nav>
    </header>

   
    <div class="wrapper">
     
    </div>
    <img alt="Vue logo" class="logo" src="@/assets/images/fondo.jpg" width="500" height="500"/>

  <RouterView />

</template>

<style scoped>
header {
  background: rgba(250, 126, 11, 0.9);
  width: 200%;
  position: center;
  z-index:200;
}
nav {
  float:inline-start; /* Desplazamos el nav hacia la izquierda */
}

nav ul {
  list-style: none;
  overflow: hidden; /* Limpiamos errores de float */
}

nav ul li {
  float:right;
  font-family: Arial, sans-serif;
  font-size: 16px;
}

nav ul li RouterLink {
  display: contents; /* Convertimos los elementos a en elementos bloque para manipular el padding */
  padding: 20px;
  color: #fff;
  text-decoration: none;
}

nav ul li:hover {
  background:transparent;
}
.logo {
  display: block;
  margin: 0 auto 5rem;
}
.contenido {
  padding-top: 80px;
}


.wrapper {

 display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
}


nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}



nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 3);
  }

  .logo {
    margin: 2 2rem 10 10;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: justify;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 0.5rem 0;
    margin-top: 0.5rem;
  }
}
</style>
