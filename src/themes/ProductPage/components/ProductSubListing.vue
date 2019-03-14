<template>
    <section class="product-sublisting-component">
    	Product sublisting
        <Sublisting>
            <section slot="sublisting-items">
                <Product v-for="(product, index) in products"
                        :key="index" 
                        :product="product"></Product>
            </section>
        </Sublisting>
    </section>
</template>

<script>
	import Product from '../../../core/Product/Product'; 
    import Sublisting from '../../../core/Layout/components/Sublisting';

    export default {
        name: 'ProductSubListing',

        props: {
            products: {
                type: Array,
                required: true
            }
        },

        components: {
            Sublisting,
        	Product
    	}
    }
</script>

<style scoped lang="less">
	section {
		border: 1px solid lightseagreen;
		padding: 5px;
	}
</style>
