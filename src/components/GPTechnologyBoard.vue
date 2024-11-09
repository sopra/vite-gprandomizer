<template>
    <div>
        <v-container>
            <v-row>
                <v-col class="terraformTech">
                    <p>
                        <span>TF:FED</span>
                        <span>TF:ADV</span>
                    </p>
                    <p>
                        <span>TF:BAS</span>
                    </p>
                </v-col>
                <v-col class="navigationTech">
                    <p>
                        <span>NAV:ADV</span>
                    </p>
                    <p>
                        <span>NAV:BAS</span>
                    </p>
                </v-col>
                <v-col>
                    <p>
                        <span>AI:ADV</span>
                    </p>
                    <p>
                        <span>AI:BAS</span>
                    </p>
                </v-col>
                <v-col >
                    <p>
                        <span>GP:ADV</span>
                    </p>
                    <p>
                        <span>GP:BAS</span>
                    </p>
                </v-col>
                <v-col >
                    <p>
                        <span>ECO:ADV</span>
                    </p>
                    <p>
                        <span>ECO:BAS</span>
                    </p>
                </v-col>
                <v-col >
                    <p>
                        <span>SCI:ADV</span>
                    </p>
                    <p>
                        <span>SCI:BAS</span>
                    </p>
                </v-col>
            </v-row>
            <v-row >
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
</style>