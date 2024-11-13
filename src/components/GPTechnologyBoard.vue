<template>
    <div>
        <v-container>
            <v-row>
                <v-col class="d-flex align-center terraformTech">
                    <v-img :lazy-src=fedTerraform.imagePath :src=fedTerraform.imagePath></v-img>
                </v-col>
                <v-col v-for="(atech, index) in aTechs" :key="index" :class="techClassList[index]">
                    <v-img :lazy-src="atech.imagePath" :src="atech.imagePath" />
                    <v-img :lazy-src="basTechs[index].imagePath" :src="basTechs[index].imagePath"></v-img>
                </v-col>
            </v-row>
            <v-row class="freeTech justify-space-evenly">
                <v-col cols="2" v-for="(btech, i) in basTechs.slice(-3)" :key="i">
                    <v-img :lazy-src="btech.imagePath" :src="btech.imagePath" ></v-img>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script>
export default {
    data: () => ({
        techClassList: [
            "terraformTech",
            "navigationTech",
            "aiTech",
            "gaiaformTech",
            "economyTech",
            "scienceTech"
        ]
    }),
    props: [
        "fedTerraform",
        "basTechs",
        "aTechs"
    ]
}
</script>

<style scoped>
.terraformTech {
    background-color: #7b4f40;
}

.navigationTech {
    background-color: #6c84a3;
}

.aiTech {
    background-color: #53a236;
}

.gaiaformTech {
    background-color: #a81974;
}

.economyTech {
    background-color: #f0a108;
}

.scienceTech {
    background-color: #1b9bcc;
}

.freeTech {
    background-color: #8b939d;
}
</style>