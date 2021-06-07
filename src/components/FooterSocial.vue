<template>
    <section>
        <div class="container">
            <!-- SUBMIT -->
            <button type="submit">Sign-Up Now!</button>
            <!-- /SUBMIT -->
            <!-- SOCIAL NETWORK -->
            <div>
                <h4>Follow Us</h4>
                <ul>
                    <li v-for="linkSocialNetwork, index in linksSocialNetwork" :key="index">
                        <a href="linkSocialNetwork.url">
                            <img :src="linkSocialNetwork.image" :alt="linkSocialNetwork.alt">
                        </a>
                    </li>
                </ul>
            </div>
            <!-- /SOCIAL NETWORK -->
        </div>
    </section>
</template>

<script>
export default {
    name: 'FooterSocial',
    data: function() {
        return {
            linksSocialNetwork: [
                {
                    image: require('../assets/img/footer-facebook.png'),
                    url: '#',
                    alt: 'Facebook'
                },
                {
                    image: require('../assets/img/footer-twitter.png'),
                    url: '#',
                    alt: 'Twitter'
                },
                {
                    image: require('../assets/img/footer-youtube.png'),
                    url: '#',
                    alt: 'Youtube'
                },
                {
                    image: require('../assets/img/footer-pinterest.png'),
                    url: '#',
                    alt: 'Pintarest'
                },
                {
                    image: require('../assets/img/footer-periscope.png'),
                    url: '#',
                    alt: 'Periscope'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/variables.scss';
    @import '../style/mixins';

    section {
        background-color: $dark-grey;

        .container {
            @include flex-positioning (space-between, center);
            padding: 25px 0;

            button {
                padding: 12px 20px;
                border: 2px solid $blue-dc;
                text-transform: uppercase;
                font-size: 15px;
                font-weight: 700;
                color: $white;
                background-color: unset;
                cursor: pointer;
                transition: background-color .3s;

                &:hover {
                    background-color: $blue-dc;
                }
            }

            div {
                display: flex;
                align-items: center;

                h4 {
                    margin-right: 30px;
                    text-transform: uppercase;
                    font-size: 16px;
                    color: $blue-dc;
                }

                ul {
                    @include links-list (row);

                    li {
                        &:not(:last-child) {
                            margin-right: 15px;
                        }

                        a {                          
                            transition: opacity .3s;

                            &:hover {
                                opacity: 0.5;
                            }
                        }
                    }
                }
            }
        }
    }
</style>