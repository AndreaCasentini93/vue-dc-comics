<template>
    <section>
        <div class="container">
            <div>
                <h4>
                    Titolo
                </h4>
                <ul>
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
    name: 'FooterLinks'
}
</script>

<style lang="scss" scoped>
    @import '../style/variables.scss';

    section {
        background: url("../assets/img/footer-bg.jpg");

        .container {
            display: flex;
            position: relative;
            min-height: 300px;
            padding: 30px;
            overflow: hidden;

            div {
                display: flex;
                flex-direction: column;
                margin-right: 50px;

                h4 {
                    margin-bottom: 15px;
                    text-transform: uppercase;
                    font-size: 15px;
                    color: $white;
                }

                ul {
                    list-style: none;

                    li {
                        a {
                            text-decoration: none;
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
                width: 400px;
                object-fit: cover;
                object-position: 0 -50px;
            }
        }
    }
</style>