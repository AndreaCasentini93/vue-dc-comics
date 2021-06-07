<template>
    <section>
        <div class="container">
            <div>
                <h4>DC Comics</h4>
                <ul>
                    <li>
                        <a href="#">Link</a>
                    </li>
                    <li>
                        <a href="#">Link</a>
                    </li>
                    <li>
                        <a href="#">Link</a>
                    </li>
                    <li>
                        <a href="#">Link</a>
                    </li>
                    <li>
                        <a href="#">Link</a>
                    </li>
                    <li>
                        <a href="#">Link</a>
                    </li>
                    <li>
                        <a href="#">Link</a>
                    </li>
                </ul>
                <h4>Shop</h4>
                <ul>
                    <li>
                        <a href="#">Link</a>
                    </li>
                    <li>
                        <a href="#">Link</a>
                    </li>
                </ul>
            </div>
            <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
    </section>
</template>

<script>
export default {
    name: 'FooterLinks',
    data: function() {
        return {
            links: [
                {
                    
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/variables.scss';

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
                    margin-top: 12px;
                    margin-bottom: 12px;
                    text-transform: uppercase;
                    font-size: 16px;
                    color: $white;
                }

                ul {
                    list-style: none;

                    li {
                        margin: 8px 0;

                        a {
                            text-decoration: none;
                            font-size: 14px;
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
                width: 580px;
                object-fit: cover;
                object-position: 0 -95px;
            }
        }
    }
</style>