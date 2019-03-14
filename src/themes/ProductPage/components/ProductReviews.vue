<template>
    <section class="product-reviews-component">
    	Product reviews
    	<ReviewsListing :reviews="reviews"></ReviewsListing>
    	<ReviewForm :actionButton="actionButton"
                    :addReviewAction="addReviewAction"></ReviewForm>
    </section>
</template>

<script>
	import ReviewsListing from '../../../core/Reviews/ReviewsListing';
	import ReviewForm from '../../../core/Reviews/Forms/ReviewForm';
 
    export default {
        name: 'ProductReviews',

        props: {
            reviews: {
                type: Array,
                required: true
            },
            actionButton: {
                type: Object,
                required: false,
                default: null
            },
            addReviewAction: {
                type: Function,
                required: false,
                default: null
            }
        },

        components: {
        	ReviewsListing,
        	ReviewForm
    	}
    }
</script>

<style scoped lang="less">
	section {
		border: 1px solid orange;
		padding: 5px;
	}
</style>
