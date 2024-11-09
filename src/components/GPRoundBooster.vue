<template>
    <v-container>
        <v-row>
            <v-col v-for="roundBoosterTile in roundBoosterTiles">
                {{ roundBoosterTile }}
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    data: () => ({
        roundBoosterTiles: [
            'RNDBOOST1-image',
            'RNDBOOST2-image',
            'RNDBOOST3-image',
            'RNDBOOST4-image',
            'RNDBOOST5-image',
            'RNDBOOST6-image',
            'RNDBOOST7-image',
        ]
    })
}
</script>

<style scoped>
</style>