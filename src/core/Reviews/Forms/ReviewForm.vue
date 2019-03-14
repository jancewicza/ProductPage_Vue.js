<template>
    <section class="review-form-component">
    	Review form
        <ActionButton 
            :classes="actionButton.classes"
            :action="actionButton.action"
            :text="actionButton.text"
            :icon="actionButton.icon"
            :type="actionButton.type"
            @action="addReviewAction"></ActionButton>
    </section>
</template>

<script>
    import ActionButton from '../../Layout/components/ActionButton';

    export default {
        name: 'ReviewForm',

        props: {
            actionButton: {
                type: Object,
                required: true
            },
            addReviewAction: {
                type: Function,
                required: true
            }
        },

        components: {
        	ActionButton
    	}
    }
</script>

<style scoped lang="less">
    .review-form-component {
        
    }
</style>
