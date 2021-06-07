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
                    text: 'Digital comics',
                    image: '../assets/img/buy-comics-digital-comics.png',
                    alt: 'Image Digital Comics',
                    url: '#'
                },
                {
                    text: 'Digital comics',
                    image: '../assets/img/buy-comics-digital-comics.png',
                    alt: 'Image Digital Comics',
                    url: '#'
                },
                {
                    text: 'Digital comics',
                    image: '../assets/img/buy-comics-digital-comics.png',
                    alt: 'Image Digital Comics',
                    url: '#'
                },
                {
                    text: 'Digital comics',
                    image: '../assets/img/buy-comics-digital-comics.png',
                    alt: 'Image Digital Comics',
                    url: '#'
                },
                {
                    text: 'Digital comics',
                    image: '../assets/img/buy-comics-digital-comics.png',
                    alt: 'Image Digital Comics',
                    url: '#'
                },
                {
                    text: 'Digital comics',
                    image: '../assets/img/buy-comics-digital-comics.png',
                    alt: 'Image Digital Comics',
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