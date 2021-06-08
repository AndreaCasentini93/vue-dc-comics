<template>
    <section>
        <div class="container">
            <div>Current Series</div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Jumbotron'
}
</script>

<style lang="scss" scoped>
    @import '../style/variables.scss';
    @import '../style/mixins';

    section {
        width: 100%;
        height: 410px;
        background-image: url("../assets/img/jumbotron.jpg");
        @include background-properties(cover, top);

        .container {
            width: 100%;
            height: 100%;
            position: relative;

            div {
                position: absolute;
                bottom: 0;
                left: 0;
                transform: translateY(50%);
                padding: 10px 20px;
                text-transform: uppercase;
                font-size: 25px;
                font-weight: 700;
                color: $white;
                background-color: $blue-dc;
            }
        }
    }
</style>