<script setup lang="ts">
    import { onMounted, ref } from 'vue';

    const count = ref(0);
    function increment() {
        count.value += 1;
    }

    onMounted(() => {
        console.log('El valor inicial del contador es ' + count.value);
    })
</script>
<template>
    <h1>Hola soy la version con Composition</h1>
    <h1>Contador: {{ count }}</h1>
    <button @click="increment">
        Incremetar contador
    </button>
</template>