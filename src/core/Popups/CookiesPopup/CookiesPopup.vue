<template>
    <section class="cookies-popup-component">
    	<BottomStickyPopup>
            <section slot="bottom-sticky-popup">
                Cookies popup
                <Link   
                    :classes="link.classes"
                    :href="link.href"
                    :text="link.text">  
                </Link>
            </section>   
        </BottomStickyPopup>
    </section>
</template>

<script>
    import BottomStickyPopup from '../components/BottomStickyPopup';
    import Link from '../../Layout/components/Link';

    export default {
        name: 'CookiesPopup',

        props: {
            link: {
                type: Object,
                required: false,
                default: null
            }
        },

        components: {
            BottomStickyPopup,
            Link
    	}
    }
</script>

<style scoped lang="less">

</style>
