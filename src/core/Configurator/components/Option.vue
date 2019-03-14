<template>
    <section class="option-component">
    	Option
    </section>
</template>

<script>
    export default {
        name: 'Option',

        props: {
            label: {
                type: String,
                required: false,
                default: ''
            },
            option: {
                type: Object,
                required: true
            },
            type: {
                type: String,
                required: true,
                validator: value => {
                    return ['select', 'number'].indexOf(value) !== -1;
                }
            },
            variants: {
                type: Object,
                required: true
            }
        }
    }
</script>

<style scoped lang="less">

</style>
