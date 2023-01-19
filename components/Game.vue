<template lang="">
    <div class="wrapper">
        <div class="game">
            <a :href="game.link" target="_blank">
                <img :src="require(`./../assets/images/${game.img}`)"></img>
            </a>
            <h2 style="text-align: center;">{{ game.title }}</h2>
            <p>{{ game.desc }}</p>
        </div>
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
    @keyframes fade-in {
        from {box-shadow: 5px 5px 50px 1px rgba(0,0,0,0.3)}
        to {box-shadow: 5px 5px 50px 1px rgba(0,0,0,0.4)}
    }
    .wrapper {
        .game {
            margin: 0 20px;
            margin-bottom: 40px;
            display: flex;
            flex-direction: column;
            align-items: center;
            img {
                width: 100%;
                height: auto;
                border-radius: 20px;
                box-shadow: 5px 5px 50px 1px rgba(0,0,0,0.3);
                &:hover {
                    animation: fade-in 0.1s linear 0s 1 normal forwards;
                }
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
    }
</style>