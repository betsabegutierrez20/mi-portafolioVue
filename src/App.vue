<script setup>
import NavBar from './components/NavBar.vue';
import DatosPersonales from './components/DatosPersonales.vue';
import EducacionComponente from './components/EducacionComponente.vue';
import ExperienciaComponente from './components/ExperienciaComponente.vue';
import ProyectosComponente from './components/ProyectosComponente.vue';
import HabillidadesComponente from './components/HabillidadesComponente.vue';
import InteresesComponente from './components/InteresesComponente.vue';

</script>

<template>
  <header id="t">
    <!--Barra de navegacion-->
    <NavBar/>
    <!--Componentes Datos Personales-->
    <DatosPersonales/>
   
  </header>
  <main>
    <!--el estilo css de secction se encuentra en base.css-->
    <section id="educacion">
      <h2>Educación - Cursos</h2>
      <!--Componente Educación-->
      <EducacionComponente/>
    </section>
    <section id="experiencia">
      <h2>Experiencia</h2>
      <!--Componete Experiencia-->
      <ExperienciaComponente/>
    </section>
    <section id="proyectos">
      <h2>Proyectos</h2>
      <ProyectosComponente/>
      <!--Componetes Proyectos-->
    </section>
    <section id="habilidades">
      <h2>Habilidades</h2>
      <HabillidadesComponente/>
    </section>
    <section id="intereses">
      <h2>Intereses</h2>
      <InteresesComponente/>
    </section>
  </main>
  <footer>
    <a href="#top">Inicio</a>
    <p> © 2024 Betsabé Daiana Gutierrez Santos - Portafolio web</p>
  </footer>
</template>

<style scoped>
footer{
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 2rem;
  font-size: 1.3rem;
}

</style>
