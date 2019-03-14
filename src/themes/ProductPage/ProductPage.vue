<template>
    <section class="product-page-component">
        <Header></Header>
        <ProductVisualisation :visualisations="product.visualisations"></ProductVisualisation>
        <Configurator   
            :options="product.options"
            :actionButton="addToCartButtonProperties"
            :actions="productActionButtons"
            :addToCartAction="addToCartAction"></Configurator>
        <ProductDetails></ProductDetails>
        <ProductReviews 
            :reviews="product.reviews"
            :actionButton="addReviewButtonProperties"
            :addReviewAction="addReviewAction"></ProductReviews>
        <ProductSublisting :products="product.crosselingProducts"></ProductSublisting>
        <Banner :banner="product.banners[0]"></Banner>
        <ProductSublisting :products="product.crosselingProducts"></ProductSublisting>
        <Footer 
            :subscribeNewsletter="true"
            :actionButton="subscribeNewsletterButtonProperties"
            :subscribeNewsletterAction="subscribeNewsletterAction"></Footer>
        <CookiesPopup :link="cookiesLinkProperties"></CookiesPopup>
    </section>
</template>

<script>
    import Header from '../../core/Layout/components/Header';
    import Footer from '../../core/Layout/components/Footer';
    import Banner from '../../core/Layout/components/Banner';
    import Configurator from '../../core/Configurator/Configurator';
    import CookiesPopup from '../../core/Popups/CookiesPopup/CookiesPopup';
    import ProductVisualisation from './components/ProductVisualisation';
    import ProductDetails from './components/ProductDetails';
    import ProductReviews from './components/ProductReviews';
	import ProductSublisting from './components/ProductSublisting';

    export default {
        name: 'ProductPage',

        data () {
            return {
                loading: false,
                product: {
                    visualisations: [
                        { 
                            picture: 'String',
                            seo: 'String' 
                        },
                        { 
                            picture: 'String',
                            seo: 'String'
                        },
                        { 
                            picture: 'String',
                            seo: 'String'
                        }
                    ],
                    options: [
                        {
                            type: 'select',
                            variants: {},
                            label: 'String'
                        },
                        {
                            type: 'number',
                            variants: {},
                            label: 'String'
                        }
                    ],
                    crosselingProducts: [
                        { product1: {} },
                        { product2: {} },
                        { product3: {} },
                        { product4: {} },
                        { product5: {} }
                    ],
                    reviews: [
                        { review1: {} },
                        { review2: {} },
                        { review3: {} },
                        { review4: {} }
                    ],
                    banners: [
                        { banner1: {} }
                    ]
                },
            }
        },

        components: {
            Header,
            Footer,
            Banner,
            Configurator,
            CookiesPopup,
            ProductVisualisation,
            ProductDetails,
            ProductReviews,
            ProductSublisting
    	},

        computed: {
            addToCartButtonProperties() {
                return {
                    classes: "btn-dark",
                    text: "Add to cart"
                }
            },

            cookiesLinkProperties() {
                return {
                    classes: "link-default",
                    href: "#",
                    text: "See details"
                }
            },

            loginLinkProperties() {
               return {
                    classes: "link-default",
                    href: "#",
                    text: "login"
                } 
            },

            productActionButtons() {
                return [
                    {
                        classes: "btn-link",
                        action: this.addToFavoriteAction,
                        text: "Add to favorite",
                        icon: 'add-to-favorite',
                        type: 'link'
                    },
                    {
                        classes: "btn-link",
                        action: this.addToCompareAction,
                        text: "Add to compare",
                        icon: 'add-to-compare',
                        type: 'link'
                    }
                ]
            },

            addReviewButtonProperties() {
                return {
                    classes: "btn-dark",
                    text: "Add review"
                }
            },

            subscribeNewsletterButtonProperties() {
                return {
                    text: "Subscribe"
                }
            }
        },

        methods: {
            addToCartAction() {
                console.log('product added to cart');
            },

            addToFavoriteAction() {
                console.log('product added to favorite');
            },

            addToCompareAction() {
                console.log('product added to compare');
            },

            addReviewAction() {
                console.log('added new review');      
            },

            subscribeNewsletterAction() {
                console.log('newsletter popup shown');
            }
        }
    }
</script>

<style scoped lang="less">
    html {
        box-sizing: border-box;
    }

	section {
		border: 1px solid red;
		padding: 5px;
	}
</style>

<style lang="less">
    .product-page-component {
        .slider-component {
            background: lightgoldenrodyellow;
        }

        section.product-component {
            background: lightpink;
        }

        section.link-component {
            text-decoration: underline;
        }
    }
</style>
