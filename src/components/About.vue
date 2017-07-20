<template>
<div id="about">
  <v-layout row wrap>
    <v-flex xs10 offset-xs1>
      <v-card id="me" class="elevation-5">
        <v-card-text>
          <h6 class="text-xs-center">About Me</h6>
          <v-layout row justify-center style="position: relative;">
            <v-btn id="butn" @click="about = true">What About You?</v-btn>
            <v-card id="pop-out" class="elevation-10" v-if="about">
              <v-card-title>
                <div class="headline ml-3">"Not all who wander are lost, but I have a terrible sense of direction"</div>
              </v-card-title>
              <v-card-media src="/static/travolta.gif" height="400px">
              </v-card-media>
              <v-card-text>
                <v-spacer></v-spacer>--- James Schultz.</v-card-text>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn id="butn" @click="about = false">Neat</v-btn>
              </v-card-actions>
            </v-card>
          </v-layout>
        </v-card-text>
      </v-card>
    </v-flex>
    <v-flex  xs10 offset-xs1>
      <v-card id="journey" class="elevation-5">
        <v-card-text>
        <h6 class="text-xs-center">The Journey</h6>
        <v-layout row justify-center style="position: relative;">
          <v-btn id="butn" @click="journey = true">Take the trip</v-btn>
          <v-card id="pop-out" class="elevation-10" v-if="journey">
            <v-card-title>
              <div class="headline ml-3">"I get blown up, but I get up again. You're never gunna keep me down"</div>
            </v-card-title>
            <v-card-media src="/static/splosion.gif" height="400px">
            </v-card-media>
            <v-card-text>---Chumbawumba</v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn id="butn" @click="journey = false">That is dark James</v-btn>
            </v-card-actions>
          </v-card>
        </v-layout>
      </v-card-text>
      </v-card>
    </v-flex>
    <v-flex  xs10 offset-xs1>
      <v-card id="project" class="elevation-5">
        <v-card-text>
        <h6 class="text-xs-center">The Problem</h6>
        <v-layout row justify-center style="position: relative;">
          <v-btn id="butn" @click="project = true">Never enough time</v-btn>
          <v-card id="pop-out" class="elevation-10" v-if="project">
            <v-card-title>
              <div class="headline ml-5">"Families are like branches on a tree. We grow in different directions, yet our roots remain the same."</div>
            </v-card-title>
            <v-card-media src="/static/ohana.gif" height="400px">
            </v-card-media>
            <v-card-text>---The Giving Tree</v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn id="butn" @click="project = false">The Good Stuff</v-btn>
            </v-card-actions>
          </v-card>
        </v-layout>
      </v-card-text>
    </v-card>
    </v-flex>
    <v-flex  xs10 offset-xs1>
      <v-card  id="tech" class="elevation-5">
        <v-card-text>
        <h6 class="text-xs-center">The Capstone Shuffle</h6>
        <v-layout row justify-center style="position: relative;">
          <v-btn id="butn" @click="tech = true">Growing Pains</v-btn>
          <v-card id="pop-out" class="elevation-10" v-if="tech">
            <v-card-title>
              <div class="headline ml-1">"I never lose. I win or I learn"</div>
            </v-card-title>
            <v-card-media src="/static/scott.gif" height="200px">
            </v-card-media>
            <v-card-text>---Michael Scott</v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn id="butn" @click="tech = false">Moving on...</v-btn>
            </v-card-actions>
          </v-card>
        </v-layout>
      </v-card-text>
    </v-card>
    </v-flex>
    <v-flex  xs10 offset-xs1>
      <v-card id="future" class="elevation-5">
        <v-card-text>
        <h6 class="text-xs-center">The Future</h6>
        <v-layout row justify-center style="position: relative;">
            <v-btn id="butn" @click="future = true">Onward</v-btn>
            <v-card id="pop-out" class="elevation-10" v-if="future">
              <v-card-title>
                <div class="headline ">"A good developer knows that a project is never done and it is never as good as you want it to be. It just needs to be good enough for production." </div>
              </v-card-title>
              <v-card-media src="/static/bug.gif" height="500px">
              </v-card-media>
              <v-card-text>---Every Senior Dev Ever</v-card-text>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn id="butn" @click="future = false">Got it</v-btn>
              </v-card-actions>
            </v-card>
        </v-layout>
      </v-card-text>
      </v-card>
    </v-flex>
    <v-flex  xs10 offset-xs1>
      <v-card id="contact" class="elevation-5">
        <v-card-text>
      <h6 class="text-xs-center"><router-link to="/DB" exact>Contact</router-link></h6>
        <v-layout row justify-center style="position: relative;">
            <v-btn id="butn" @click="contact = true">You could just yell...</v-btn>
            <v-card id="pop-out" class="elevation-10" v-if="contact">
              <v-card-title>
                <div class="headline">"How lucky am I to have something that makes saying goodbye so hard"</div>
              </v-card-title>
              <v-card-text>---Pooh Bear</v-card-text>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn id="butn" @click="contact= false">Big Finish</v-btn>
              </v-card-actions>
            </v-card>
        </v-layout>
        </v-card-text>
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


#butn {
background: #FF8A65;
}
#pop-out{
  text-align: center;
  background-color: #656565;
}
</style>
