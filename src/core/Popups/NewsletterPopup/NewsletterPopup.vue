<template>
    <section class="newsletter-popup-component">
    	<CenterStickyPopup>
            <section slot="center-sticky-popup">
                Newsletter popup
            </section>    
        </CenterStickyPopup>
    </section>
</template>

<script>
	import CenterStickyPopup from '../components/CenterStickyPopup';

    export default {
        name: 'NewsletterPopup',
        
        components: {
        	CenterStickyPopup
    	}
    }
</script>

<style scoped lang="less">

</style>
