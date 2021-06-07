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
            justify-content: space-between;
            padding: 30px;

            div {
                display: flex;
                flex-direction: column;
                margin-right: 50px;

                h4 {
                    color: $white;
                }

                ul {
                    list-style: none;

                    li {
                        a {
                            text-decoration: none;
                        }
                    }
                }
            }

            img {
                width: 300px;
                object-position: 0 -50px;
            }
        }
    }
</style>