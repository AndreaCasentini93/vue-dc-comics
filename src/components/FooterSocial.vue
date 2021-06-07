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
                        <a href="linkSocialNetwork.url"><i :class="linkSocialNetwork.class"></i></a>
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
                    class: 'fab fa-facebook-f',
                    url: '#',
                },
                {
                    class: 'fab fa-twitter',
                    url: '#',
                },
                {
                    class: 'fab fa-youtube',
                    url: '#',
                },
                {
                    class: 'fab fa-pinterest-p',
                    url: '#',
                },
                {
                    class: 'fas fa-map-marker-alt',
                    url: '#',
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/variables.scss';

    section {
        background-color: $dark-grey;

        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
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
                    display: flex;
                    list-style: none;

                    li {
                        &:not(:last-child) {
                            margin-right: 15px;
                        }

                        a {  
                            display: flex;
                            justify-content: center;
                            align-items: center;
                            width: 40px;
                            height: 40px;  
                            border-radius: 50%;                       
                            text-decoration: unset;
                            font-size: 16px;
                            color: $dark-grey;
                            background-color: $light-grey;
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