<template>
    <v-container>
        <v-row class="roundboosterArea">
            <v-col v-for="roundBoosterTile in roundBoosterTiles" v-bind:key="roundBoosterTile.id">
                {{ roundBoosterTile.description }}
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    data: () => ({
        roundBoosterTiles: [
            {
                id: 'RNDBOOSTER1',
                description: 'Round Booster #1',
                imageUrl: 'pic/RND'
            },
            {
                id: 'RNDBOOSTER2',
                description: 'Round Booster #2',
                imageUrl: 'pic/RND'
            },
            {
                id: 'RNDBOOSTER3',
                description: 'Round Booster #3',
                imageUrl: 'pic/RND'
            },
            {
                id: 'RNDBOOSTER4',
                description: 'Round Booster #4',
                imageUrl: 'pic/RND'
            },
            {
                id: 'RNDBOOSTER5',
                description: 'Round Booster #5',
                imageUrl: 'pic/RND'
            },
            {
                id: 'RNDBOOSTER6',
                description: 'Round Booster #6',
                imageUrl: 'pic/RND'
            },
            {
                id: 'RNDBOOSTER7',
                description: 'Round Booster #7',
                imageUrl: 'pic/RND'
            },
        ]
    })
}
</script>

<style scoped>
.roundboosterArea {
    background-color: #8b939d;
}
</style>