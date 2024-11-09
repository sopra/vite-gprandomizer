<template>
        <v-main>
            <p>
                <v-select :items="playerNumber" label="Players" v-model="selected">
                    {{ selected }}
                </v-select>
            </p>
            <p>
                <v-btn-toggle v-model="expansionFlag" flat>
                    <v-btn elevation="2">Normal Map</v-btn>
                    <v-btn elevation="2">Lost Fleet Map</v-btn>
                </v-btn-toggle>
            </p>
            <GPTechnologyBoardVue />
            <GPMapVue />
        </v-main>
</template>

<script>
import GPMapVue from "./GPMap.vue";
import GPRoundBoardVue from './GPRoundBoard.vue';
import GPRoundBoosterVue from './GPRoundBooster.vue';
import GPTechnologyBoardVue from './GPTechnologyBoard.vue';

export default {
    data: () => ({
        playerNumber: [
            '2',
            '3',
            '4'],
        selected: [ '4' ],
        expansionFlag: "",
    })
}
</script>

<style>

</style>