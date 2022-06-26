<template>
    <div class="games">
        <Game v-for="game in gamesList" :game="game" :key="game.name"/>
    </div>
</template>

<script lang="ts">
import { games } from "./../data/data"
import Game from "./Game.vue"
export default {
    data() {
        // console.log(games)
        return {
            gamesList: games
        };
    },
    components: { Game }
}
</script>

<style lang="scss" scoped>
    .games {
        width: 100%;
        display: flex;
        justify-content: flex-start;
        gap: 60px;
    }
</style>