<template>
    <div class="container">
        <div class="row">
            <div class="col-md-7">
							<div class="row">
								<div :key="product.id" class="col-md-6" v-for="product in products">
									<Product 
										:product="product"
										v-on:add-to-card="addToCart(product)">
									</Product>
								</div>
							</div>
						</div>
            <div class="col-md-5"></div>
        </div>
    </div>
</template>

<script>
import products from '@/products.json'
import Product from '@/components/Product.vue'

export default {
  name: 'app',
	components: {
		Product
	},
	data() {
		return {
			products,
			cart: []
		}	
	},
	methods: {
		addToCart(product) {
			console.log(product)	
		}
	}
}
</script>

