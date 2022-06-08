<template>
    <h1>Estamos en Autos</h1>
    <!-- Aqui obtenemos los datos de la url para saber que auto mostrar por parametro -->
    <p>{{ $route.params.name }}</p>

    <button @click="load">Cargar</button>
</template>

<script>
import { useRoute, useRouter } from "vue-router";
export default {
    setup() {
        // Aqui obtenemos los datos de la url para saber que auto mostrar por script
        const route = useRoute();
        const router = useRouter();
        console.log("router");

        // console.log("load");
        const load = () => {
            console.log("ejecutando peticion");
            setTimeout(() => {
                console.log("Volver a Home...");
                router.push("/");
            }, 1000);
        };
    },
};
</script>

<style></style>
