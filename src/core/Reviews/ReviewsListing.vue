<template>
    <section class="reviews-listing-component">
    	Reviews listing
    	<ReviewItem 
            v-for="(review, index) in reviews"
            :key="index"></ReviewItem>
    </section>
</template>

<script>
	import ReviewItem from './components/ReviewItem';

    export default {
        name: 'ReviewsListing',

        props: {
            reviews: {
                type: Array,
                required: true
            }
        },

    	components: {
        	ReviewItem
    	}
    }
</script>

<style scoped lang="less">
	section {
		border: 1px solid violet;
		padding: 5px;
	}
</style>