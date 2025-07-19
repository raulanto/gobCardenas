
<script setup lang="ts">
import tiempoCorazon from "~/components/tiempoCorazon.vue";
import BotonFrases from "~/components/botonFrases.vue";
</script>




<template>
    <main class="relative h-screen w-full overflow-hidden">
        <!-- Fondo con imagen -->
        <div class="absolute inset-0 z-0">
            <img
                src="~/assets/50846162-a-background-of-falling-red-hearts-over-a-white-background.jpg"
                alt="Fondo de corazones"
                class="w-full h-full object-cover object-center"
            >
            <!-- Capa de overlay opcional para mejor legibilidad -->
            <div class=""></div>
        </div>

        <!-- Contenido centrado -->
        <section class="relative z-10 container mx-auto h-full flex flex-col justify-center items-center px-4">
            <tiempo-corazon class="w-full max-w-4xl"></tiempo-corazon>
            <boton-frases/>
        </section>
    </main>
</template>

<style>

</style>