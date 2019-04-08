<template>
    <v-container>
        <v-card flat>
            <v-toolbar color="primary" dark extended flat>
                <v-toolbar-side-icon></v-toolbar-side-icon>
            </v-toolbar>
            <v-container grid-list-lg>
                <v-layout row pb-2>
                    <v-flex hidden-md-and-down lg3>
                        <Sidebar />
                    </v-flex>
                    <v-flex md12 lg9>
                        <v-card class="card--flex-toolbar">
                            <v-toolbar card prominent>
                                <v-toolbar-title class="body-2 grey--text">{{$page.title}}</v-toolbar-title>

                                <v-spacer></v-spacer>

                                <v-btn icon>
                                    <v-icon>search</v-icon>
                                </v-btn>

                                <v-btn icon>
                                    <v-icon>apps</v-icon>
                                </v-btn>

                                <v-btn icon>
                                    <v-icon>more_vert</v-icon>
                                </v-btn>
                            </v-toolbar>

                            <v-divider></v-divider>

                            <v-card-text>
                                <Content />
                            </v-card-text>
                        </v-card>
                        <br />
                    </v-flex>
                </v-layout>
            </v-container>
        </v-card>
    </v-container>
</template>
<style>
@media screen and (min-width: 900px) {
    .card--flex-toolbar {
        margin-top: -88px;
    }
}
@media screen and (max-width: 899px) {
    .card--flex-toolbar {
        margin-top: -60px;
    }
}

</style>