<template>
    <section>
        <div class="container">
            <Cards v-for="volume, index in volumes" :key="index" :card="volume"/>
            <button type="input">Load More</button>
        </div>
    </section>
</template>

<script>
import Cards from './Cards.vue';
import DcComics from '../data/dc-comics.js'

export default {
    name: 'DcVolumes',
    components: {
        Cards,
    },
    data: function() {
        return {
            volumes: DcComics
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/variables.scss';
    @import '../style/mixins';

    section {
        width: 100%;
        background-color: darken($dark-grey, 8%);

        .container {
            padding: 25px 0 20px 0;
            @include flex-centering ('horizontal');
            flex-wrap: wrap;
            align-content: flex-start;

            button {
                padding: 10px 50px;
                border: 2px solid $blue-dc;
                margin-top: 20px;
                text-transform: uppercase;
                font-size: 14px;
                font-weight: 700;
                color: $white;
                background-color: $blue-dc;
                cursor: pointer;
                transition: background-color .3s;

                &:hover {
                    background-color: rgba($blue-dc, 0);
                }
            }
        }
    }
</style>