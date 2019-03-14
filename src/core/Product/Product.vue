<template>
    <section class="product-component">
    	Product
    </section>
</template>

<script>
    export default {
        name: 'Product',

        props: {
            product: {
                type: Object,
                required: true
            }
        }
    }
</script>

<style scoped lang="less">
    section {
        background: lightgreen;
    }
</style>
