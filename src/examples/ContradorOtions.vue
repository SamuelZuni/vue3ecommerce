<script lang="ts">
    export default {
        data() {
            return {
                count: 0
            }
        },
        methods: {
            increase() {
                this.count += 1;
            },
            decrease() {
                this.count -= 1;
            }
        },
        mounted() {
            console.log('El valor inicial del contador es ' + this.count);
        }
    }    
</script>

<template>
    <p>Objetivo: tienes que llegar a 20 clicks</p>

    <h1>Contador: {{ count }}</h1>
    <button @click="increase">
        Aumentar Contador
    </button>
    <button @click="decrease">
        Restar Contador
    </button>
    <p v-if="count <= 10">Vamos tu puedes!</p>
    <p v-else>Ya te falta muy poco...</p>
</template>