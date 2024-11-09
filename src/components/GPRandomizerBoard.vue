<template>
        <v-main>
            <v-container>
                <v-row class="justify-center">
                    <v-col cols="4" lg="5" md="6" sm="8" xs="12">
                        <div>
                            <v-select :items="playerNumber" label="Players" v-model="selected">
                                {{ selected }}
                            </v-select>
                        </div>
                    </v-col>
                </v-row>
                <v-row class="justify-center">
                    <v-col cols="3">
                        <v-btn block elevation="4" @click="setupOriginal">Original Setup</v-btn>
                    </v-col>
                    <v-col cols="3">
                        <v-btn block elevation="4" @click="setupLostFleet">Lost Fleet Setup</v-btn>
                    </v-col>
                </v-row>
            </v-container>
            <GPTechnologyBoardVue />
            <GPRoundBoardVue />
            <GPRoundBoosterVue />
            <GPLostFleetVue />
            <v-container>
                <v-row class="justify-center">
                    <v-col xs="12" sm="12" md="6" lg="4">
                        <v-btn block @click="generateMap">GenerateMap</v-btn>
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
        selected: '4',
        expansionFlag: "",
    }),
    methods: {
        setupOriginal() {
        },
        setupLostFleet() {
        },
        generateMap() {
        }
    }
}
</script>

<style scoped>


</style>