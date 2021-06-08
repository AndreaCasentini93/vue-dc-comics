<template>
    <div>
        <img :src="card.thumb" :alt="card.series">
        <h6>{{ card.series }}</h6>
    </div>
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

    div {
        width: calc((100% / 6) - 30px);
        margin: 15px;

        img {
            display: block;
            width: 100%;
            height: 170px;
            margin-bottom: 20px;
            object-fit: cover;
            object-position: top;
        }

        h6 {
            margin-bottom: 15px;
            text-transform: uppercase;
            font-weight: 400;
            font-size: 12px;
            color: $white;
        }
    }
</style>