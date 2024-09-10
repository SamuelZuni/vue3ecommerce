<script lang="ts">
import type { PropType } from 'vue';
import type { Product } from '../model/types';
    export default {
        props: {
            product: {
                type: Object as PropType<Product>,
                    required:true
                }
        },
        emits: ['addProduct'],
        methods: {
            onAddButtonClick() {
                //console.log('agregando producto ' + this.product.id);
                this.$emit('addProduct');
            }
        }
    }    
</script>

<template>
    <v-card >
        <v-img
        color="surface-variant"
        height="200"
        src="https://cdn.vuetifyjs.com/docs/images/cards/purple-flowers.jpg"
        cover />
        
        <v-card-title>
            {{ product.name }}
        </v-card-title>

        <v-card-text>
            <p class="mb-4">
                Es precio de ejemplo
            </p>
            <v-chip>
                $ {{ product.price }}
            </v-chip>
        </v-card-text>

        <v-card-actions>
            <v-btn @click="onAddButtonClick" color="orange-lighten-2">Agregar al carrito</v-btn>
        </v-card-actions>
    </v-card>
</template>