<template>
    <v-main>
        <v-container>
            <v-row class="justify-center">
                <v-col cols="4" lg="5" md="6" sm="8" xs="12">
                    <div>
                        <v-select :items="playerNumber" label="Players" v-model="selectedPlayerNumber">
                            {{ selectedPlayerNumber }}
                        </v-select>
                    </div>
                </v-col>
            </v-row>
            <v-row class="justify-center">
                <v-col lg="3" md="4" sm="6" xs="6">
                    <v-btn block @click="setupOriginal">Original Setup</v-btn>
                </v-col>
                <v-col lg="3" md="4" sm="6" xs="6">
                    <v-btn block @click="setupLostFleet">Lost Fleet Setup</v-btn>
                </v-col>
            </v-row>
        </v-container>
        <GPTechnologyBoardVue :fedTerraform=federationOfTerraformTechnology :basTechs=basicTechsForTechBoard />
        <GPRoundBoardVue :rts="roundTiles" :fsts="finalscoreTiles" :rbts="roundboosterTiles"/>
        <GPLostFleetVue />
        <v-container>
            <v-row class="justify-center">
                <v-col xs="12" sm="12" md="6" lg="4">
                    <v-btn block @click="generateMap">Generate Map</v-btn>
                </v-col>
            </v-row>
        </v-container>
        <GPMapVue />
    </v-main>
</template>

<script>
import GPMapVue from "./GPMap.vue";
import GPRoundBoardVue from './GPRoundBoard.vue';
import GPRoundBoosterVue from './GPRoundBooster.vue';
import GPTechnologyBoardVue from './GPTechnologyBoard.vue';
import GPLostFleetVue from "./GPLostFleet.vue";
import GPFooter from "./GPFooter.vue";

import Federations from "../assets/data/federations.json";
import BasicTechnologies from "../assets/data/basicTechnologies.json";
import AdvancedTechnologies from "../assets/data/advancedTechnologies.json";
import Rounds from "../assets/data/roundTiles.json"
import FinalScores from "../assets/data/finalscoreTiles.json"
import RoundBoosters from "../assets/data/roundboosterTiles.json"


export default {
    components: {
        GPTechnologyBoardVue,
        GPRoundBoardVue,
        GPRoundBoosterVue,
        GPLostFleetVue,
        GPMapVue,
        GPFooter
    },
    data: () => ({
        playerNumber: [
            '2',
            '3',
            '4'],
        selectedPlayerNumber: '4',
        expansionFlag: "",
        federations: Federations,
        federationOfTerraformTechnology: {},
        basicTechs: BasicTechnologies,
        basicTechsForTechBoard: [],
        advTechs: AdvancedTechnologies,
        rounds: Rounds,
        roundTiles: [],
        finals: FinalScores,
        finalscoreTiles: [],
        roundboosters: RoundBoosters,
        roundboosterTiles: [],
    }),
    methods: {
        setupOriginal() {
            const filterType = "origin";
            this.setup(filterType)

            // select federation tile for terraform technology
            this.federationOfTerraformTechnology =
                this.shuffle(this.federations.items.filter((e) => e.type === filterType))[0]

            // 
            this.basicTechsForTechBoard = this.shuffle(this.basicTechs.items.filter((e) => e.type === filterType))
            const advtechs = this.shuffle(this.advTechs.items.filter((e) => e.type === filterType)).slice(0, 5)

            advtechs.forEach((e) => {
            });

            // select round tiles.
            this.roundTiles = this.shuffle(
                this.rounds.items.filter((e) => e.type === filterType)
            ).slice(0, 6)

            // select final scores.
            this.finalscoreTiles = this.shuffle(
                this.finals.items.filter((e) => e.type === filterType)
            ).slice(0, 2)

            // select roundboosters
            console.log(this.selectedPlayerNumber)
            this.roundboosterTiles = this.shuffle(
                this.roundboosters.items.filter((e) => e.type === filterType)
            ).slice(0, parseInt(this.selectedPlayerNumber, 10) + 3)
        },
        setupLostFleet() {
        },
        generateMap() {
        },
        setup(filterType) {
        },
        shuffle(array) {
            for (let i = array.length - 1; i > 0; i--) {
                let r = Math.floor(Math.random() * (i + 1));
                let tmp = array[i];
                array[i] = array[r];
                array[r] = tmp;
            }

            return array;
        },
    },
    beforeMount() {
    }
}
</script>

<style scoped>
</style>