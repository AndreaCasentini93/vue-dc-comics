<template>
    <header>
        <div class="container">
            <nav>
                <!-- LOGO -->
                <a href="#">
                    <img src="../assets/img/dc-logo.png" alt="Logo">
                </a>
                <!-- /LOGO -->
                <!-- LINKS -->
                <ul>
                    <li v-for="link, index in links" :key="index">
                        <a :href="link.url" :class="{ active: link.current }">{{ link.text }}</a>
                    </li>
                </ul>
                <!-- /LINKS -->
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data: function() {
        return {
            links: [
                {
                    text: 'Characters',
                    url: '#',
                    current: false
                },
                {
                    text: 'Comics',
                    url: '#',
                    current: true
                },
                {
                    text: 'Movies',
                    url: '#',
                    current: false
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false
                },
                {
                    text: 'Games',
                    url: '#',
                    current: false
                },
                {
                    text: 'Collectibles',
                    url: '#',
                    current: false
                },
                {
                    text: 'Videos',
                    url: '#',
                    current: false
                },
                {
                    text: 'Fans',
                    url: '#',
                    current: false
                },
                {
                    text: 'News',
                    url: '#',
                    current: false
                },
                {
                    text: 'Shop',
                    url: '#',
                    current: false
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/variables';

    header {
        background-color: $white;

        .container {
            nav {
                display: flex;
                justify-content: space-between;
                align-items: center;

                a {
                    img {
                        max-width: 80px;
                    }
                }

                ul {
                    display: flex;
                    list-style: none;

                    li {
                        display: flex;

                        a {
                            padding: 55px 0;
                            border-bottom: 4px solid #ffffff00;
                            margin: 0 18px;
                            text-transform: uppercase;
                            text-decoration: none;
                            font-size: 13px;
                            font-weight: 700;
                            color: $dark-grey;
                            transition: color .3s, border .3s;

                            &:hover,
                            &.active {
                                color: $blue-dc;
                                border-bottom: 4px solid $blue-dc;
                            }
                        }
                    }
                }
            }
        }
    }
</style>