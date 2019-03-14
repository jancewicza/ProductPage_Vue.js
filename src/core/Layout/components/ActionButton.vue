<template>
    <section class="action-button-component">
    	<button
            :class="['btn', classes]"
            @click="$emit('action')">
            {{ text }}
        </button>
    </section>
</template>

<script>   
    export default {
        name: 'ActionButton',

        props: {
            classes: {
                type: String,
                required: false,
                default: 'btn-default'
            },
            text: {
                type: String,
                required: true
            },
            icon: {
                type: String,
                required: false,
                default: ''
            },
            type: {
                type: String,
                required: false,
                defalut: 'button',
                validator: value => {
                    return ['button', 'link'].indexOf(value) !== -1;
                }
            }
        }
    }
</script>

<style scoped lang="less">
	button.btn {

	}

	button.btn-default {

	}

	button.btn-dark {

	}
</style>
