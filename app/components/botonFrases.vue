<template>
    <div class="romantic-container">
        <button @click="mostrarFraseRomantica" class="romantic-button">
            Mago y Raul
        </button>
        <div v-if="fraseActual" class="frase-romantica">
            "{{ fraseActual }}"
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const frasesRomanticas = ref([
    "Eres el sueño que mi corazón no quiere dejar de soñar.",
    "Si te preguntan por mí, diles que me perdí en tus ojos y no quiero que me encuentren.",
    "El amor no se mira, se siente. Y yo cuando te veo, siento mariposas en mi alma.",
    "Eres la razón por la que mi corazón late más fuerte cada mañana.",
    "No necesito mirar las estrellas cuando tengo tu mirada iluminando mi vida.",
    "Si el amor fuera un viaje, yo querría perderme contigo para siempre.",
    "Eres la melodía que mi corazón repite en silencio todo el día.",
    "De todas las historias de amor, la mía favorita es la que estoy escribiendo contigo.",
    "No existe en el diccionario una palabra que defina lo que siento por ti.",
    "El mejor momento de mi día es cuando nuestros caminos se cruzan.",
    "Te amo mi princesa hermosa",
    "Eres mi Princesa hermosa",
]);

const fraseActual = ref('');

const mostrarFraseRomantica = () => {
    const frasesDisponibles = frasesRomanticas.value.filter(frase => frase !== fraseActual.value);
    const indiceAleatorio = Math.floor(Math.random() * frasesDisponibles.length);
    fraseActual.value = frasesDisponibles[indiceAleatorio];
};
</script>

<style scoped>
.romantic-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
    padding: 20px;
    font-family: 'Arial', sans-serif;
}

.romantic-button {
    padding: 12px 24px;
    background-color: #ff6b81;
    color: white;
    border: none;
    border-radius: 25px;
    font-size: 16px;
    cursor: pointer;
    transition: all 0.3s ease;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.romantic-button:hover {
    background-color: #ff4757;
    transform: translateY(-2px);
    box-shadow: 0 6px 8px rgba(0, 0, 0, 0.15);
}

.romantic-button:active {
    transform: translateY(1px);
}

.frase-romantica {
    padding: 15px 25px;
    background-color: #fff0f3;
    border-radius: 10px;
    max-width: 80%;
    text-align: center;
    font-style: italic;
    font-size: 18px;
    color: #333;
    border-left: 4px solid #ff6b81;
    animation: fadeIn 0.5s ease;
}

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
}
</style>