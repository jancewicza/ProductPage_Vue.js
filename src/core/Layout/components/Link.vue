<template>
    <section class="link-component">
    	<a
            :class="['link', classes]"
            :href="href">
            <i v-if="icon" :class="icon"></i>
            {{ text }}
        </a>
    </section>
</template>

<script>
    export default {
        name: 'Link',

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
            href: {
                type: String,
                required: true
            },
            icon: {
                type: String,
                required: false,
                default: ''
            }
        },
    }
</script>

<style scoped lang="less">
	.link {

	}

	.link.link-default {

	}
</style>
