<script lang="ts">
import ProductCard from './ProductCard.vue';
import Cart from './Cart.vue';
import type { CartDetail, Product } from '../model/types'; 

export default {
        components: {
            ProductCard,
            Cart
        },
        data() {
            return {
                products: <Array<Product>>[
                    {name: 'Silla', price: 56, id: 1},
                    {name: 'Monitor', price: 343, id: 2},
                    {name: 'Micrófono', price: 124, id: 3},
                ],
                details: <Array<CartDetail>>[]
            }
        },
        methods: {
            onAddProduct(productId: number) {
                const detailFound = this.details.find(d => d.productId == productId);
                
                if (detailFound) {
                    detailFound.quantity += 1;
                } else {

                    this.details.push({
                        productId,
                        quantity: 1
                    });
                }
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
        
    <Cart :details="details"/>
</template>