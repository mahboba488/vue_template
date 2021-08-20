<template>
<nav>
    <v-navigation-drawer v-model="right" dark app class="deep-orange accent-2" fixed right>
        <v-layout column align-center>
            <v-flex class="mt-5">
                <v-avatar size="100">
                    <img src="/231.png" alt="">

                </v-avatar>
                <h4 class="white--text subheading mt-1 text-center">MahbobaZaman</h4>
                <h5 class="white--text subheading mt-1 text-center">CEO.Skill jobs</h5>


            </v-flex>

        </v-layout>

        <p class ="white--text subheading pl-3 mt-3">
            Rank of company

        </p>
        <v-list rounded dense>
            <v-list-item router to="/">
                <v-list-item-action>
                    03
                </v-list-item-action>
                <v-list-item-content>
                    <v-list-item-title>
                        The Income
                    </v-list-item-title>
                </v-list-item-content>
            </v-list-item>
             <v-list-item router to="/">
                <v-list-item-action>
                    05
                </v-list-item-action>
                <v-list-item-content>
                    <v-list-item-title>
                        Human Resources
                    </v-list-item-title>
                </v-list-item-content>
            </v-list-item>
             <v-list-item router to="/">
                <v-list-item-action>
                    12
                </v-list-item-action>
                <v-list-item-content>
                    <v-list-item-title>
                        The Income
                    </v-list-item-title>
                </v-list-item-content>
            </v-list-item>

        </v-list>
        <p class="white--text subheading pl-3 mt-3">
            Next Meeting Places

        </p>

        <v-timeline align-top dense fill-dot small dark>
            <v-timeline-item fill-dot small color="white" class="white--text">
                Norisseeberg

            </v-timeline-item>
            <v-timeline-item fill-dot small color="white" class="white--text">
                Norisseeberg

            </v-timeline-item>
            <v-timeline-item fill-dot small color="white" class="white--text">
                Norisseeberg

            </v-timeline-item>

        </v-timeline>

    </v-navigation-drawer>
</nav>
</template>
<script>
export default {
    name:"Rightnav"
}
</script>