<template>
  <div class="project">
    <h1 class="subheading grey--text">project</h1>
    <v-container>
      <v-layout row wrap class="mb-4">
        <v-tooltip bottom>
          <template v-slot:activator="{ on }">
            <v-btn small outlined color="green" @click="sortBy('title')" class="mr-2" dark v-on="on">
              <v-icon left small>folder</v-icon>
              <span class="caption text-lower">By project Title</span>
            </v-btn>
              
          </template>
          <span>sort project</span>
        </v-tooltip>
        <v-tooltip bottom>
          <template v-slot:activator="{ on }">
            <v-btn small outlined color="green" @click="sortBy('person')" class="mr-2" dark v-on="on">
              <v-icon left small>person</v-icon>
              <span class="caption text-lower">By name</span>
            </v-btn>
              
          </template>
          <span>sort person</span>
        </v-tooltip>
      </v-layout>
      <v-card flat v-for="pro in project" :key="pro.title" class="mb-1">
        <v-layout row wrap:class="`pa-3 pro ${pro.status}`">
          <v-flex xs-12 md6>
            <div class="caption grey--text">person</div>
            <div>{{pro.person}}</div>

          </v-flex>
          <v-flex xs-6 sm4 md2>
            <div class="caption grey--text">due By</div>
            <div>{{pro.due}}</div>
             
          </v-flex>

        </v-layout>

      </v-card>
    </v-container>

  </div>
</template>

<script>
export default {
  data:() =>({
    project:[
      {title:'site web', person: 'khaled',due:'10/10/2020',status:'complete'},
      {title:'Application Mobile', person: 'Iyad',due:'2/07/2020',status:'complete'},
      {title:'Gestion de stock', person: 'Zineb',due:'1/1/2021',status:'yes'},
      {title:'conception', person: 'Mick',due:'5/4/2021',status:'up'},

    ]
  }),
  methods: {
    sortBy(prop){
      this.project.sort((a,b) => a[prop]< b[prop] ? -1:1)
    }
  },
}
</script>
<style>
.pro.complete{
  border-left:4px solid #3cd1c2;
}
.pro.on{
    border-left:4px solid orange;

}

.pro.up{
    border-left:4px solid red;

}

.pro.yes{
    border-left:4px solid yellow;

}

</style>
