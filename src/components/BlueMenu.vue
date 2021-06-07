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
                    image: '../assets/img/buy-comics-digital-comics.png',
                    alt: 'Image Digital Comics',
                    url: '#'
                },
                {
                    text: 'DC Merchandise',
                    image: '../assets/img/buy-comics-digital-comics.png',
                    alt: 'Image DC Merchandise',
                    url: '#'
                },
                {
                    text: 'Subscription',
                    image: '../assets/img/buy-comics-digital-comics.png',
                    alt: 'Image Subscription',
                    url: '#'
                },
                {
                    text: 'Comic Shop Locator',
                    image: '../assets/img/buy-comics-digital-comics.png',
                    alt: 'Image Comic Shop Locator',
                    url: '#'
                },
                {
                    text: 'DC Power Visa',
                    image: '../assets/img/buy-comics-digital-comics.png',
                    alt: 'Image DC Power Visa',
                    url: '#'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scope>
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
                    a {
                        display: flex;
                        align-items: center;
                        text-decoration: none;
                        color: $white;

                        img {
                            width: 45px;
                            margin-right: 15px;
                        }

                        div {
                            text-transform: uppercase;
                            font-size: 14px;
                        }
                    }
                }
            }
        }
    }
</style>