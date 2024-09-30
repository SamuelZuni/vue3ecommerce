<script lang="ts">
import ProductCard from './ProductCard.vue';
import Cart from './Cart.vue';
import type { CartDetail, Product } from '../model/types'; 


export default {
        components: {
            ProductCard,
            Cart
        },
        props: ['details'],
        data() {
            return {
                products: <Array<Product>>[
                    {name: 'Silla', price: 56, id: 1},
                    {name: 'Monitor', price: 343, id: 2},
                    {name: 'Micrófono', price: 124, id: 3},
                ]
            }
        },
        methods: {
            onAddProduct(productId: number) {
                
            }
        }
    }    
</script>

<template>
    <v-row>
    <v-col v-for="p in products" cols="4">
        <ProductCard 
        :product="p"
        @addProduct="onAddProduct(p.id)" />
    </v-col>
    </v-row>
        
    <Cart details! />
</template>