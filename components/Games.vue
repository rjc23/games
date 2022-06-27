<template>
    <div>
        <div class="wrapper">
            <div class="games">
                <Game v-for="game in gamesList" :game="game" :key="game.id"/>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { games } from "./../data/data"
import Game from "./Game.vue"
export default {
    data() {
        return {
            gamesList: games
        };
    },
    components: { Game }
}
</script>

<style lang="scss" scoped>
    @import './../assets/scss/responsive.scss';
    .wrapper {
        width: 100%;
        display: flex;
        justify-content: center;
        .games {
            width: 100%;
            max-width: 1200px;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            & * {
                width: 50%;
                @include respond-to(tablet) {
                    width: 25%;
                }
            }
        }
    }
</style>