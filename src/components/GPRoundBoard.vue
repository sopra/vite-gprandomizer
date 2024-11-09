<template>
    <v-container>
        <v-row>
            <v-col cols="2" v-for="(roundTile, index) in roundScoreTiles" :key="index" class="roundtile">
                {{ roundTile }}
            </v-col>
        </v-row>
        <v-row>
            <v-col class="finalscore">
                <div v-for="(finalScoreTile, index) in finalScoreTiles" :key="index">
                    {{  finalScoreTile }}
                </div>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    data: () => ({
        roundScoreTiles: [
            'RND1-image',
            'RND2-image',
            'RND3-image',
            'RND4-image',
            'RND5-image',
            'RND6-image',
        ],
        finalScoreTiles: [
            'FIN1-image',
            'FIN2-image'
        ]
    }),
    props: [
    ]
}
</script>

<style scoped>
.roundtile {
    background-color: black;
    color: white;
}

.finalscore {
    background-color: #04833a;
}
</style>