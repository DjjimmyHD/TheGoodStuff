  <template>

<nav>
    <div class="nav-wrapper">

      <h1 class="brand-logo center">The Good Stuff</h1>
      <ul>
        <li><router-link to="/" exact>Home</router-link></li>
        <li><router-link to="/GoodStuff" exact>Good Stuff</router-link></li>
        <li><router-link to="/DB" exact>Add Event</router-link></li>
        <li><router-link to="/About" exact>About the Project</router-link></li>

      </ul>
    </div>
  </nav>

  </template>

<script>
export default {
  name: 'top-nav',
  data () {
    return {

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >
.nav-wrapper{
  background-color: #FF8A65;
}


</style>
