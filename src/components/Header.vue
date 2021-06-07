<template>
    <header>
        <div class="container">
            <nav>
                <a href="#">
                    <img src="../assets/img/dc-logo.png" alt="Logo">
                </a>
                <ul>
                    <li>
                        <a href="#">ciao</a>
                    </li>
                    <li>
                        <a href="#">ciao</a>
                    </li>
                    <li>
                        <a  class="active" href="#">ciao</a>
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