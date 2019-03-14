<template>
    <section class="configurator-component">
    	<Breadcrumbs></Breadcrumbs>
    	<ConfigurationForm  
            :actionButton="actionButton"
            :options="options"
            :actions="actions"
            :addToCartAction="addToCartAction">
        </ConfigurationForm>
    </section>
</template>

<script>
	import Breadcrumbs from '../Layout/components/Breadcrumbs';
	import ConfigurationForm from './Forms/ConfigurationForm';

    export default {
        name: 'Configurator',
        
        props: {
            actionButton: {
                type: Object,
                required: true
            },
            actions: {
                type: Array,
                required: true
            },
            options: {
                type: Array,
                required: false
            },
            addToCartAction: {
                type: Function,
                required: true
            }
        },

        components: {
        	Breadcrumbs,
        	ConfigurationForm
    	}
    }
</script>

<style scoped lang="less">
    section {
        border: 1px solid antiquewhite;
        padding: 5px;
    }
</style>
