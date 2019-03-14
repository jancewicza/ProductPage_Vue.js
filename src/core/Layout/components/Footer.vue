<template>
    <section class="footer-component">
    	<SubscribeNewsletter 
            v-if="subscribeNewsletter"
            :actionButton="actionButton"
            :subscribeNewsletterAction="subscribeNewsletterAction">
        </SubscribeNewsletter>
        Footer elements
    </section>
</template>

<script>
  import SubscribeNewsletter from '../../Newsletter/SubscribeNewsletter';

    export default {
        name: 'Footer',

        props: {
            subscribeNewsletter: {
                type: Boolean,
                required: false,
                default: false
            },
            actionButton: {
                type: Object,
                required: false,
                default: null
            },
            subscribeNewsletterAction: {
                type: Function,
                required: true
            }
        },

        components: {
        	SubscribeNewsletter
    	}
    }
</script>

<style scoped lang="less">
    section {
        border: 1px solid pink;
        padding: 5px;
    }
</style>
