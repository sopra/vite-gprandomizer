<template>
    <v-container>
        <v-row no-gutter>
            <v-col cols="2" v-for="(roundTile, index) in rts" :key="index" class="roundtile text-center">
                <p>Round: {{ index+1 }}</p>
            </v-col>
        </v-row>
        <v-row>
            <v-col cols="2" v-for="(roundTile, index) in rts" :key="index" class="roundtile">
                <v-img :lazy-src=roundTile.imagePath :src=roundTile.imagePath></v-img>
            </v-col>
        </v-row>
        <v-row class="justify-center">
            <v-col cols="2" class="finalscore">
                <v-img v-for="(fst, index) in fsts" :key="index"
                :lazy-src=fst.imagePath :src=fst.imagePath ></v-img>
            </v-col>
            <v-col v-for="(rbt, index) in rbts" :key="index" class="roundbooster">
                <v-img
                    :razy-src=rbt.imagePath :src=rbt.imagePath max-height="230" ></v-img>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    data: () => ({
    }),
    props: [
        "rts",
        "fsts",
        "rbts"
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

.roundbooster {
    background-color: #8b939d;
}
</style>