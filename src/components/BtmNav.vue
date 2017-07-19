<template>

  <v-footer id="btm-nav" class="pa-3">
    <h6 class="white--text">"The Good Stuff" is a James Schultz Creation</h6>

    <v-spacer></v-spacer>
    <h6 class="white--text">© {{ new Date().getFullYear() }}</h6>

  </v-footer>



</template>


<script>
export default {
  name: 'btm-nav',
  data () {
    return {

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
#btm-nav{
  height: 100%;
  background-color: #FF8A65;
}





</style>
