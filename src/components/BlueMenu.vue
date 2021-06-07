<template>
    <section>
        <div class="container">
            <ul>
                <li v-for="link, index in links" :key="index">
                    <a :href="link.url">
                        <img :src="link.image" :alt="link.alt">
                        <div>{{ link.text }}</div>
                    </a>
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
export default {
    name: 'BlueMenu',
    data: function() {
        return {
            links: [
                {
                    text: 'Digital Comics',
                    image: require('../assets/img/buy-comics-digital-comics.png'),
                    alt: 'Image Digital Comics',
                    url: '#'
                },
                {
                    text: 'DC Merchandise',
                    image: require('../assets/img/buy-comics-merchandise.png'),
                    alt: 'Image DC Merchandise',
                    url: '#'
                },
                {
                    text: 'Subscription',
                    image: require('../assets/img/buy-comics-subscriptions.png'),
                    alt: 'Image Subscription',
                    url: '#'
                },
                {
                    text: 'Comic Shop Locator',
                    image: require('../assets/img/buy-comics-shop-locator.png'),
                    alt: 'Image Comic Shop Locator',
                    url: '#'
                },
                {
                    text: 'DC Power Visa',
                    image: require('../assets/img/buy-dc-power-visa.svg'),
                    alt: 'Image DC Power Visa',
                    url: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/variables.scss';

    section {
        background-color: $blue-dc;

        .container {
            ul {
                display: flex;
                justify-content: space-around;
                align-items: center;
                list-style: none;
                padding: 30px;

                li {
                    margin: 0 30px;

                    a {
                        display: flex;
                        align-items: center;
                        text-decoration: none;
                        color: $white;

                        img {
                            max-width: 50px;
                            max-height: 50px;
                            margin-right: 10px;
                        }

                        div {
                            text-transform: uppercase;
                            font-size: 13px;
                            white-space: nowrap;
                        }
                    }
                }
            }
        }
    }
</style>