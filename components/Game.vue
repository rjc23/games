<template>
    <div class="game">
        <a :href="game.link" target="_blank">
            <nuxt-img :src="game.img"></nuxt-img>
        </a>
        <h2>{{ game.title }}</h2>
        <p>{{ game.desc }}</p>
    </div>
</template>

<script lang="ts">
    import { PropType } from "vue";
    import { Game } from "~/interfaces/interfaces";

    export default {
        props: {
            game: {
                type: Object as PropType<Game>
            }
        },
    }
</script>

<style lang="scss" scoped>
    .game {
        display: flex;
        flex-direction: column;
        // justify-content: center;
        align-items: center;
        width: 260px;
        img {
            height: 260px;
            width: 260px;
            border-radius: 20px;
            box-shadow: 5px 5px 50px 1px rgba(0,0,0,0.5);
        }
        h2 {
            font-family: 'Space Mono';
            font-weight: 700;
        }
        p {
            font-family: 'Space Mono';
            margin: 0;
            text-align: center;
        }
    }
</style>