<template>


      <v-layout row>
        <v-flex xs12 sm6 offset-sm3>
          <v-card>
            <v-toolbar class="cyan" dark>
              <v-toolbar-title>Event List</v-toolbar-title>
            </v-toolbar>
            <v-list two-line>
              <template v-for="item in items">
                <v-subheader v-if="item.header" v-text="item.header"></v-subheader>
                <v-divider v-else-if="item.divider" v-bind:inset="item.inset"></v-divider>
                <v-list-tile avatar v-else v-bind:key="item.title" href="javascript:;" download target="_blank">
                  <v-list-tile-content>
                    <v-list-tile-title v-html="item.title"></v-list-tile-title>
                    <v-list-tile-sub-title v-html="item.date"></v-list-tile-sub-title>
                  </v-list-tile-content>
                </v-list-tile>
              </template>
            </v-list>
          </v-card>
        </v-flex>
      </v-layout>





</template>

<script>
export default {
name: 'message',
data () {
  return {
    items:[]

  }
},  created() {
        this.$http.get('https://capstone-endpoint.firebaseio.com/.json').then(function(data){
            return data.json()
        }).then(function(data){
            var eventsArray = [];
            for (let key in data){
                data[key].id = key;
                eventsArray.push(data[key]);
            }
            this.items = eventsArray;
            console.log(this.items);
        });
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>




</style>
