<template>
    <section class="product-visualisation-component">
    	Product visualisation
    	<Slider :items="productVisualisationProperties"></Slider>
    </section>
</template>

<script>
    import Slider from '../../../core/Layout/components/Slider';

    export default {
        name: 'ProductVisualisation',

        props: {
            visualisations: {
                type: Array,
                required: true
            },
            zoom: {
                type: Boolean,
                required: false,
                default: true                
            }
        },

        components: {
            Slider
    	},

        computed: {
            productVisualisationProperties() {
                return this.visualisations.map(visualisation => {
                    return visualisation.picture;
                });
            }
        },
    }
</script>

<style scoped lang="less">
    section {
        border: 1px solid lightslategray;
        padding: 5px;
    }
</style>
