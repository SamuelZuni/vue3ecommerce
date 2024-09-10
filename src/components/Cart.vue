<script lang="ts">
import type { PropType } from 'vue';
import type { CartDetail } from '../model/types';
    export default {
        props: {
            details: {
                type: Object as PropType<Array<CartDetail>>,
                required: true
            }
        },
    }
</script>

 
<template>
    <v-card class="mt-4">
        <v-card-text>
            <v-card-title>
                Productos agregados al carrito
            </v-card-title>
            <v-list>
                <v-list-item v-for="detail in details" :value="detail.productId">
                    Product {{ detail.productId }}  (Qty: {{ detail.quantity }})
                </v-list-item>
            </v-list>
        </v-card-text>
    </v-card>
</template>