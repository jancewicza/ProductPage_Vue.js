<template>
    <section class="slider-component">
    	<article 
            v-for="(item, index) in items"
            :key="index">
            Slider item {{ item }}
        </article>
    </section>
</template>

<script>
    export default {
        name: 'Slider',

        props: {
            items: {
                type: Array,
                required: true
            },
            slideNavigation: {
                type: Boolean,
                required: false,
                default: true
            },
            bottomNavigation: {
                type: Boolean,
                required: false,
                default: true
            }
        }
    }
</script>

<style scoped lang="less">
    section {
        border: 1px solid lightblue;
        padding: 5px;
    }
</style>