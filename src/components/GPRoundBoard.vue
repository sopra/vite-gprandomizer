<template>
    <v-container>
        <v-row>
            <v-col v-for="(roundTile, index) in roundScoreTiles" :key="index">
                {{ roundTile }}
            </v-col>
            <v-col>
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
</style>