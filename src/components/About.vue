<template>

  <div id="about">

    <v-layout row wrap>
      <v-flex xs12>
        <v-card id="me" class="elevation-5">
        <v-card-text>
          <p class="text-xs-center">About Me</p>

          <v-layout row justify-center style="position: relative;">
             <v-dialog v-model="meow" lazy absolute>
               <v-btn primary dark slot="activator">Where I started</v-btn>
               <v-card>
                 <v-card-title>
                   <div class="headline">Rocky Mountain High Colorado</div>
                 </v-card-title>
                 <v-card-text>"Not all who wander are lost, but I have a terrible sense of direction" <v-spacer></v-spacer>--- James Schultz.</v-card-text>
                 <v-card-actions>
                   <v-spacer></v-spacer>

                   <v-btn class="green--text darken-1" flat="flat" @click.native="meow = false">Neat</v-btn>
                 </v-card-actions>
               </v-card>
             </v-dialog>
           </v-layout>


        </v-card-text>
        </v-card>


      </v-flex>
      <v-flex xs12>
        <v-card id="journey">
          <v-card-text>My Journey</v-card-text>
          <v-layout row justify-center style="position: relative;">
             <v-dialog v-model="cheese" lazy absolute>
               <v-btn primary dark slot="activator">Take the trip</v-btn>
               <v-card>
                 <v-card-title>
                   <div class="headline">I've worn a lot of hats none of them fit</div>
                 </v-card-title>
                 <v-card-text>"Life is about the journey, about appreciating the struggle. It doesnt matter how you get there as long as you get there."</v-card-text>
                 <v-card-actions>
                   <v-spacer></v-spacer>

                   <v-btn class="green--text darken-1" flat="flat" @click.native="cheese = false">That's neat</v-btn>
                 </v-card-actions>
               </v-card>
             </v-dialog>
           </v-layout>
        </v-card>
      </v-flex>
      <v-flex xs12>
        <v-card id="project">
          <v-card-text>The Problem</v-card-text>
          <v-layout row justify-center style="position: relative;">
             <v-dialog v-model="James" lazy absolute>
               <v-btn primary dark slot="activator">What is it?</v-btn>
               <v-card>
                 <v-card-title>
                   <div class="headline">Not enough time for meaningful conversation</div>
                 </v-card-title>
                 <v-card-text>The good stuff is a way to share the improtant things in your life with the important people in your life</v-card-text>
                 <v-card-actions>
                   <v-spacer></v-spacer>

                   <v-btn class="green--text darken-1" flat="flat" @click.native="James = false">Got it</v-btn>
                 </v-card-actions>
               </v-card>
             </v-dialog>
           </v-layout>
        </v-card>
      </v-flex>
      <v-flex xs12>
        <v-card id="tech">
          <v-card-text>The Capstone Shuffle</v-card-text>
          <v-layout row justify-center style="position: relative;">
             <v-dialog v-model="stuff" lazy absolute>
               <v-btn primary dark slot="activator">Growing Pains</v-btn>
               <v-card>
                 <v-card-title>
                   <div class="headline">So much to learn so little time</div>
                 </v-card-title>
                 <v-card-text>"I never lose, I win or I learn" ---Michael Scott</v-card-text>
                 <v-card-actions>
                   <v-spacer></v-spacer>

                   <v-btn class="green--text darken-1" flat="flat" @click.native="stuff = false">Got it</v-btn>
                 </v-card-actions>
               </v-card>
             </v-dialog>
           </v-layout>
        </v-card>
      </v-flex>
      <v-flex xs12>
        <v-card id="future">
          <v-card-text>The Future</v-card-text>
          <v-layout row justify-center style="position: relative;">
             <v-dialog v-model="peaches" lazy absolute>
               <v-btn primary dark slot="activator">Looking forward</v-btn>
               <v-card>
                 <v-card-title>
                   <div class="headline">Use Vuex and Build A SQL DB</div>
                 </v-card-title>
                 <v-card-text>I am passionate about this app I want to continue to work on it</v-card-text>
                 <v-card-actions>
                   <v-spacer></v-spacer>

                   <v-btn class="green--text darken-1" flat="flat" @click.native="peaches = false">Got it</v-btn>
                 </v-card-actions>
               </v-card>
             </v-dialog>
           </v-layout>
        </v-card>
      </v-flex>
      <v-flex xs12>
        <v-card id="future">
          <v-card-text>Contact Me</v-card-text>
          <v-layout row justify-center style="position: relative;">
             <v-dialog v-model="contact" lazy absolute>
               <v-btn primary dark slot="activator">You could just yell..</v-btn>
               <v-card>
                 <v-card-title>
                   <div class="headline">James Schultz</div>
                   <div class="headline">LinkedIn /ninjames101</div>
                   <div class="headline">Github /ninjames101</div>
                   <div class="headline">ninjames101.ninja</div>
                 </v-card-title>
                 <v-card-text>"How lucky am I to have something that makes saying goodbye so hard"</v-card-text>
                 <v-card-actions>
                   <v-spacer></v-spacer>

                   <v-btn class="green--text darken-1" flat="flat" @click.native="contact = false">Got it</v-btn>
                 </v-card-actions>
               </v-card>
             </v-dialog>
           </v-layout>
        </v-card>
      </v-flex>
    </v-layout>
  </div>

</template>


<script>
export default {
  name: 'about',
  data () {
    return {
      test: true,
      meow: false,
      cheese: false,
      James: false,
      stuff: false,
      peaches: false,
      contact: false,


    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#about {
  display: flex;
  min-height: 100vh;
  flex-direction: column;
  color: #20BF55;
  text-align: center;
}
#me, #journey, #project, #tech, #future {
  background-color: #F2EFEA;
}



</style>
