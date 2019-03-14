<template>
    <section class="subscribe-newsletter-component">
        Subscribe newsletter
        <ActionButton   
            :classes="actionButton.classes"
            @action="subscribeNewsletterButtonAction"
            :text="actionButton.text"
            :icon="actionButton.icon"
            :type="actionButton.type"></ActionButton>
    	<NewsletterPopup v-if="showNewsletterPopup"></NewsletterPopup>
    </section>
</template>

<script>
    import NewsletterPopup from '../Popups/NewsletterPopup/NewsletterPopup';
    import ActionButton from '../Layout/components/ActionButton';

    export default {
        name: 'SubscribeNewsletter',

        props: {
            actionButton: {
                type: Object,
                required: true
            },
            subscribeNewsletterAction: {
                type: Function,
                required: true
            }
        },

        data () {
            return {
                showNewsletterPopup: false
            }
        },

        components: {
            ActionButton,
            NewsletterPopup
    	},

        methods: {
            subscribeNewsletterButtonAction() {
                this.showNewsletterPopup = true;
                this.subscribeNewsletterAction();
            }
        }
    }
</script>

<style scoped lang="less">
    section {
        border: 1px solid green;
        padding: 5px;
    }
</style>
