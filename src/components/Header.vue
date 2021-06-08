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
                    <li v-for="link, index in links" :key="index" :class="{ active: link.current }">
                        <a :href="link.url">{{ link.text }}</a>
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
    @import '../style/mixins';

    header {
        background-color: $white;

        .container {
            nav {
                @include flex-positioning (space-between, center);

                a {
                    img {
                        max-width: 75px;
                    }
                }

                ul {
                    @include links-list (row);

                    li {
                        display: flex;
                        padding: 50px 0;
                        border-bottom: 5px solid rgba($white, 0);
                        margin: 0 18px;
                        transition: border .3s;

                        &:hover,
                        &.active {
                            border-bottom: 5px solid $blue-dc;
                        }

                        &.active a {
                            color: $blue-dc;
                        }

                        a {
                            text-transform: uppercase;
                            font-size: 13px;
                            font-weight: 700;
                            color: $dark-grey;
                            transition: color .3s;

                            &:hover {
                                color: $blue-dc;
                            }
                        }
                    }
                }
            }
        }
    }
</style>