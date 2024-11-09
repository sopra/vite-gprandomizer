<template>
    <div>
        <v-container>
            <v-row>
                <v-col class="d-flex align-center terraformTech">
                    <v-img lazy-src="/public/img/FEDcre.webp" src="/public/img/FEDcre.webp"></v-img>
                </v-col>
                <v-col class="terraformTech">
                    <v-img lazy-src="/public/img/ADVlab.webp" src="/public/img/ADVlab.webp" />
                    <v-img lazy-src="/public/img/TECcre.webp" src="/public/img/TECcre.webp" />
                </v-col>
                <v-col class="navigationTech">
                    <v-img lazy-src="/public/img/ADVstp.webp" src="/public/img/ADVstp.webp" />
                    <v-img lazy-src="/public/img/TECknw.webp" src="/public/img/TECknw.webp" />
                </v-col>
                <v-col class="aiTech">
                    <p>
                        <span>AI:ADV</span>
                    </p>
                    <p>
                        <span>AI:BAS</span>
                    </p>
                </v-col>
                <v-col class="gaiaformTech">
                    <p>
                        <span>GP:ADV</span>
                    </p>
                    <p>
                        <span>GP:BAS</span>
                    </p>
                </v-col>
                <v-col class="economyTech">
                    <p>
                        <span>ECO:ADV</span>
                    </p>
                    <p>
                        <span>ECO:BAS</span>
                    </p>
                </v-col>
                <v-col class="scienceTech">
                    <p>
                        <span>SCI:ADV</span>
                    </p>
                    <p>
                        <span>SCI:BAS</span>
                    </p>
                </v-col>
            </v-row>
            <v-row class="freeTech">
                <v-col>
                    <p>
                        <span>FREE:BAS1</span>
                    </p>
                </v-col>
                <v-col>
                    <p>
                        <span>FREE:BAS2</span>
                    </p>
                </v-col>
                <v-col>
                    <p>
                        <span>FREE:BAS3</span>
                    </p>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script>
export default {
    data: () => ({
        FED: "",
        ADVTech: [],
        BASTech: [],
        FREETech: []
    }),
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