<template>
    <header>
        <div class="container">
            <nav>
                <a href="#">
                    <img src="../assets/img/dc-logo.png" alt="Logo">
                </a>
                <ul>
                    <li v-for="link, index in links" :key="index">
                        <a :href="link.url">{{ link.text }}</a>
                    </li>
                </ul>
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
                    current: false
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
                },
            ]
        }
    }
}
</script>

<style lang="scss" scope>
    @import '../style/variables';

    header {
        background-color: #FFFFFF;

        .container {
            nav {
                display: flex;
                justify-content: space-between;
                align-items: center;

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
                            color: $header-nav-color;

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