<template>
<div id="about">
  <v-layout row wrap>
    <v-flex xs12>
      <v-card id="me" class="elevation-5">
        <v-card-text>
          <h6 class="text-xs-center">About Me</h6>
          <v-layout row justify-center style="position: relative;">
            <v-btn primary dark @click="about = true">Take the trip</v-btn>
            <v-card v-if="about">
              <v-card-title>
                <div class="headline">Rocky Mountain High Colorado</div>
              </v-card-title>
              <v-card-text>"Not all who wander are lost, but I have a terrible sense of direction"
                <v-spacer></v-spacer>--- James Schultz.</v-card-text>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn class="green--text darken-1" flat="flat" @click="about = false">Neat</v-btn>
              </v-card-actions>
            </v-card>
          </v-layout>
        </v-card-text>
      </v-card>
    </v-flex>
    <v-flex xs12>
      <v-card id="journey">
        <v-card-text>My Journey</v-card-text>
        <v-layout row justify-center style="position: relative;">
          <v-btn primary dark @click="journey = true">Take the trip</v-btn>
          <v-card v-if="journey">
            <v-card-title>
              <div class="headline">I've worn a lot of hats none of them fit</div>
            </v-card-title>
            <v-card-text>"Life is about the journey, about appreciating the struggle. It doesnt matter how you get there as long as you get there."</v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn class="green--text darken-1" flat="flat" @click="journey = false">That's neat</v-btn>
            </v-card-actions>
          </v-card>
        </v-layout>
      </v-card>
    </v-flex>
    <v-flex xs12>
      <v-card id="project">
        <v-card-text>The Problem</v-card-text>
        <v-layout row justify-center style="position: relative;">
          <v-btn primary dark @click="project = true">What is it?</v-btn>
          <v-card v-if="project">
            <v-card-title>
              <div class="headline">Not enough time for meaningful conversation</div>
            </v-card-title>
            <v-card-text>The good stuff is a way to share the improtant things in your life with the important people in your life</v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn class="green--text darken-1" flat="flat" @click="project = false">Got it</v-btn>
            </v-card-actions>
          </v-card>
        </v-layout>
      </v-card>
    </v-flex>
    <v-flex xs12>
      <v-card id="tech">
        <v-card-text>The Capstone Shuffle</v-card-text>
        <v-layout row justify-center style="position: relative;">
          <v-btn primary dark @click="tech = true">Growing Pains</v-btn>
          <v-card v-if="tech">
            <v-card-title>
              <div class="headline">So much to learn so little time</div>
            </v-card-title>
            <v-card-text>"I never lose, I win or I learn" ---Michael Scott</v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn class="green--text darken-1" flat="flat" @click="tech = false">Got it</v-btn>
            </v-card-actions>
          </v-card>
        </v-layout>
      </v-card>
    </v-flex>
    <v-flex xs12>
      <v-card id="future">
        <v-card-text>The Future</v-card-text>
        <v-layout row justify-center style="position: relative;">
            <v-btn primary dark @click="future = true">Looking forward</v-btn>
            <v-card v-if="future">
              <v-card-title>
                <div class="headline">Use Vuex and Build A SQL DB</div>
              </v-card-title>
              <v-card-text>I am passionate about this app I want to continue to work on it</v-card-text>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn class="green--text darken-1" flat="flat" @click="future = false">Got it</v-btn>
              </v-card-actions>
            </v-card>
        </v-layout>
      </v-card>
    </v-flex>
    <v-flex xs12>
      <v-card id="contact">
        <v-card-text>Contact Me</v-card-text>
        <v-layout row justify-center style="position: relative;">
            <v-btn primary dark @click="contact = true">You could just yell..</v-btn>
            <v-card v-if="contact">
              <v-card-title>
                <div class="headline">James Schultz</div>
                <div class="headline">LinkedIn /ninjames101</div>
                <div class="headline">Github /ninjames101</div>
                <div class="headline">ninjames101.ninja</div>
              </v-card-title>
              <v-card-text>"How lucky am I to have something that makes saying goodbye so hard"</v-card-text>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn class="green--text darken-1" flat="flat" @click.native="contact= false">Got it</v-btn>
              </v-card-actions>
            </v-card>
        </v-layout>
      </v-card>
    </v-flex>
  </v-layout>
</div>
</template>


<script>
export default {
  name: 'about',
  data() {
    return {
      about: false,
      journey: false,
      project: false,
      tech: false,
      future:false,
      contact: false


    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#about,
h6 {
  color: #20BF55;
  text-align: center;
}

#me,
#journey,
#project,
#tech,
#future,
#contact {
  background-color: #F2EFEA;
}

v-btn {
  background-color: black;
}
</style>
