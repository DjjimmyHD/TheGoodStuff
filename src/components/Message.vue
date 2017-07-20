<template>


      <v-layout row>
        <v-flex xs12 sm6 offset-sm3>
          <v-card id="event-card">
            <v-toolbar id="event-top">
              <v-toolbar-title>Event List</v-toolbar-title>
            </v-toolbar>
            <v-list two-line>
              <template v-for="item in items">
                <v-subheader id="title" v-text="item.title"></v-subheader>
                <v-list-tile avatar v-bind:key="item.title" href="javascript:;" download target="_blank">
                  <v-list-tile-content>
                    <v-list-tile-title id="content" v-html="item.content"></v-list-tile-title>
                    <v-list-tile-sub-title id="date" v-html="item.date"></v-list-tile-sub-title>
                    <v-list-tile-sub-title id="author" v-html="item.author"></v-list-tile-sub-title>
                  </v-list-tile-content>
                </v-list-tile>
                <v-card-text></v-card-text>
              </template>
            </v-list>
            <v-card-text>

          </v-card-text>
        </v-card>
        </v-flex>
      </v-layout>





</template>

<script>
export default {
name: 'message',
data () {
  return {
    items:[],
    inset:true,
    divider:true



  }
},  created() {
        this.$http.get('https://capstone-endpoint.firebaseio.com/.json').then(function(data){
          console.log(data);
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

#event-top{
background-color: #FF8A65;

}
#event-card{
  background-color: #F2EFEA;
}
#content{
  font-size: 20px;
  /*color: #20BF55;*/
  color: #FF8A65;

}
#date {
  font-size: 20px;
  color: #FF8A65;
}
#title {
  font-size: 20px;
  color: #656565;
}
#author {
  font-size: 20px;

}


</style>
