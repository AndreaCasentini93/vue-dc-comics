<template>
    <section>
        <div class="container">
            <!-- COLUMN 1 -->
            <div>
                <h4>DC Comics</h4>
                <ul>
                    <li v-for="linkDcComics, index in linksDcComics" :key="index">
                        <a :href="linkDcComics.url">{{ linkDcComics.text }}</a>
                    </li>
                </ul>
                <h4>Shop</h4>
                <ul>
                    <li v-for="linkShop, index in linksShop" :key="index">
                        <a :href="linkShop.url">{{ linkShop.text }}</a>
                    </li>
                </ul>
            </div>
            <!-- /COLUMN 1 -->
            <!-- COLUMN 1 -->
            <div>
                <h4>DC</h4>
                <ul>
                    <li v-for="linkDc, index in linksDc" :key="index">
                        <a :href="linkDc.url">{{ linkDc.text }}</a>
                    </li>
                </ul>
            </div>
            <!-- /COLUMN 1 -->
            <!-- COLUMN 1 -->
            <div>
                <h4>Sites</h4>
                <ul>
                    <li v-for="linkSites, index in linksSites" :key="index">
                        <a :href="linkSites.url">{{ linkSites.text }}</a>
                    </li>
                </ul>
            </div>
            <!-- /COLUMN 1 -->
            <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
    </section>
</template>

<script>
export default {
    name: 'FooterLinks',
    data: function() {
        return {
            linksDcComics: [
                {
                    text: 'Characters',
                    url: '#'
                },
                {
                    text: 'Comics',
                    url: '#'
                },
                {
                    text: 'Movies',
                    url: '#'
                },
                {
                    text: 'TV',
                    url: '#'
                },
                {
                    text: 'Games',
                    url: '#'
                },
                {
                    text: 'Videos',
                    url: '#'
                },
                {
                    text: 'News',
                    url: '#'
                }
            ],
            linksShop: [
                {
                    text: 'Shop DC',
                    url: '#'
                },
                {
                    text: 'Shop DC Collectibles',
                    url: '#'
                }
            ],
            linksDc: [
                {
                    text: 'Terms Of Use',
                    url: '#'
                },
                {
                    text: 'Privacy Policy (New)',
                    url: '#'
                },
                {
                    text: 'Ad Choices',
                    url: '#'
                },
                {
                    text: 'Advertising',
                    url: '#'
                },
                {
                    text: 'Jobs',
                    url: '#'
                },
                {
                    text: 'Subscriptions',
                    url: '#'
                },
                {
                    text: 'Talent Workshop',
                    url: '#'
                },
                {
                    text: 'CPSC Certificates',
                    url: '#'
                },
                {
                    text: 'Ratings',
                    url: '#'
                },
                {
                    text: 'Shop Help',
                    url: '#'
                },
                {
                    text: 'Contact Us',
                    url: '#'
                }
            ],
            linksSites: [
                {
                    text: 'DC',
                    url: '#'
                },
                {
                    text: 'MAD Magazine',
                    url: '#'
                },
                {
                    text: 'DC Kids',
                    url: '#'
                },
                {
                    text: 'DC Universe',
                    url: '#'
                },
                {
                    text: 'DC Power Visa',
                    url: '#'
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
        background: url("../assets/img/footer-bg.jpg");
        background-size: cover;

        .container {
            display: flex;
            position: relative;
            min-height: 320px;
            padding: 30px 0;
            overflow: hidden;

            div {
                display: flex;
                flex-direction: column;
                margin-right: 50px;

                h4 {
                    margin-top: 15px;
                    margin-bottom: 8px;
                    text-transform: uppercase;
                    font-size: 16px;
                    color: $white;
                }

                ul {
                    @include links-list (column);

                    li {
                        margin: 3px 0;

                        a {
                            font-size: 13px;
                            color: $light-grey;
                            transition: color .3s;

                            &:hover {
                                color: $blue-dc;
                            }
                        }
                    }
                }
            }
            img {
                position: absolute;
                top: 0;
                right: 0;
                width: 600px;
                object-fit: cover;
                object-position: 0 -100px;
            }
        }
    }
</style>