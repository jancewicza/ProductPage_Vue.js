<template>
    <section class="configuration-form-component">
    	Configuration form
        <Option 
            v-if="options"
            v-for="(option, index) in options"
            :key="index"
            :option="option"
            :type="option.type"
            :variants="option.variants">  
        </Option>
    	<ActionButton   
            :classes="actionButton.classes"
            @action="addToCartAction"
            :text="actionButton.text"
            :type="actionButton.type"
            :icon="actionButton.icon"> 
        </ActionButton>
        <section>
            <ActionButton
                v-for="(action, index) in actions" 
                :key="index"  
                :classes="action.classes"
                @action="action.action"
                :text="action.text"
                :icon="action.icon"
                :type="action.type">
            </ActionButton>
        </section>
    </section>
</template>

<script>
    import Option from '../components/Option';
    import ActionButton from '../../Layout/components/ActionButton';
    import Link from '../../Layout/components/Link';

    export default {
        name: 'ConfigurationForm',

        props: {
            options: {
                type: Array,
                required: false
            },
            actionButton: {
                type: Object,
                required: true
            },
            actions: {
                type: Array,
                required: false,
                default: null
            },
            addToCartAction: {
                type: Function,
                required: true
            }
        },

        components: {
            Option,
            ActionButton,
            Link
    	}
    }
</script>

<style scoped lang="less">

</style>
