<template>
    <a :href="card.thumb">
        <img :src="card.thumb" :alt="card.series">
        <h6>{{ card.series }}</h6>
    </a>
</template>

<script>
export default {
    name: 'Cards',
    props: {
        card: Object
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/variables.scss';
    @import '../style/mixins';

    a {
        width: calc((100% / 6) - 30px);
        margin: 20px 15px;
        text-decoration: none;

        &:hover > img {
            opacity: 0.5;
        }
        &:hover > h6 {
            color: $blue-dc;
        }

        img {
            display: block;
            width: 100%;
            height: 170px;
            margin-bottom: 20px;
            object-fit: cover;
            object-position: top;
            transition: opacity .3s;
        }

        h6 {
            text-transform: uppercase;
            font-weight: 400;
            font-size: 12px;
            color: $white;
            transition: color .3s;
        }
    }
</style>