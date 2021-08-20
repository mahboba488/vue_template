<template>
<nav>
    <v-app-bar color="red" dark app>
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"> </v-app-bar-nav-icon>

        <v-toolbar-title class="text-uppercase">
            <span class="font-weight-light">add</span>
            <span>IdeaPro</span>
        </v-toolbar-title>
        <v-spacer></v-spacer>
        <v-menu offset-y>
            <template v-slot:activator="{ on }">
                <v-btn text v-on="on">
                    <v-icon left>expand_more</v-icon>
                    <span>Menu</span>
                </v-btn>
            </template>
            <v-list flat>
                <v-list-item v-for="link in links" :key="link.text" router :to="link.route">
                    <v-list-item-title class="grey--text">{{ link.text }}</v-list-item-title>

                </v-list-item>
            </v-list>
        </v-menu>
        <v-btn text>
            <span>Exit</span>
            <v-icon right>exit_to_app</v-icon>
        </v-btn>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" dark app class="red darken-4">
        <v-layout column align-center>
            <v-flex class="mt-5">
                <v-avatar size="100">
                    <v-img src="/231.png"></v-img>
                </v-avatar>
                <p class="white--text subheading mt-1 text-center">MahbobaZaman</p>
            </v-flex>
            <v-flex class="mt-4 mb-4">
                <popup />
            </v-flex>
        </v-layout>
        <v-list flat>
            <v-list-item v-for="link in links" :key="link.text" router :to="link.route">
                <v-list-item-acion>
                    <v-icon class="white--text">{{ link.icon }}</v-icon>
                </v-list-item-acion>
                <v-list-item-content>
                    <v-list-item-title class="white--text">{{ link.text }}</v-list-item-title>
                </v-list-item-content>
            </v-list-item>
        </v-list>
    </v-navigation-drawer>
</nav>
</template>

<script>
import Popup from "./Popup.vue";
export default {
    data: () => ({
        drawer: true,
        links: [{
                icon: "dashboard",
                text: "Dashboard",
                route: "/",
            },
            {
                icon: "folder",
                text: "My project",
                route: "/project",
            },
            {
                icon: "person",
                text: "Team",
                route: "/team",
            },
        ],
    }),
    components: {
        Popup,
    },
};
</script>

<style scoped></style>
