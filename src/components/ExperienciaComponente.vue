<!--eslint-disable vue/multi-word-component-names-->
<script setup>
import { ref } from 'vue';
const titulo = 'Desarrollador Full Stack';
const fecha = 'Desde Enero 2024 / Julio 2025';
const experiencias = ref([
    { id: 1, src:'/src/assets/venta.svg', parrafo: 'En mi trayectoria como desarrolladora web principiante, he diseñado una página estética que demuestra mi capacidad para aplicar los conocimientos adquiridos en el aula a proyectos reales. Esta experiencia ha mejorado mis habilidades en HTML, CSS y JavaScript, y me ha permitido entender mejor la importancia de la experiencia del usuario y el diseño responsivo' },
    { id: 2, src:'/src/assets/datos_nuevos.svg', parrafo: 'He diseñado una página web intuitiva y funcional, que combina una estética moderna con una navegación fluida para ofrecer una experiencia de usuario óptima.' },
    { id: 3, src:'/src/assets/estado.svg', parrafo: 'Lideré un equipo de 4 desarrolladores en la creación de una plataforma de comercio que incrementó las ventas en un 35% durante el primer año. ' },

]);
</script>

<template>
    <div class="card">
        <h3 class="titulo">{{ titulo.toLocaleUpperCase() }}</h3>
        <p class="fecha">{{ fecha }}</p>
        <ul class="listado">
            <li class="item" v-for="experencia in experiencias" :key="experencia.id">
                <img class="imagen-svg" :src="experencia.src" width="45rem" :alt="experencia.parrafo">
                <p>{{ experencia.parrafo }}</p>
            </li>
            <!--
            <li class="item"><img class="imagen-svg" src="/src/assets/venta.svg" width="45rem" alt="">
                <p>Lideré un equipo de 5 desarrolladores en la creación de una plataforma de comercio electrónico que incrementó las ventas en un 35% durante el primer año.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/datos_nuevos.svg" width="45rem" alt="">
                <p>Diseñé y desarrollé aplicaciones web utilizando Node.js, React y MongoDB, logrando reducir el tiempo de carga de las páginas en un 50%.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/estado.svg" width="45rem" alt="">
                <p>Implementé soluciones de autenticación y autorización, mejorando la seguridad del sitio web y reduciendo los intentos de acceso no autorizado en un 20%.</p>
            </li>-->
            
        </ul>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: rgb(28, 41, 52);
    border-radius: 15px;
}

.titulo {
    font-size: 1.5rem;
    color: coral;
}

.fecha {
    font-size: 1rem;
    color: burlywood;
    margin-bottom: 1rem;
}

.listado {
    display: flex;
    flex-direction: column;
}

.item {
    align-items: center;
    display: flex;
    padding: 1rem;
    gap: 1.5rem;
}
</style>