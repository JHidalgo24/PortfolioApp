<template>
  <v-app>
    <v-main>
      <v-app-bar color="white" elevation="0">
        <h2 style="color:black; text-align: left;font-weight: bold"> My Portfolio</h2>
        <v-spacer></v-spacer>
        <v-btn icon @click="dis = 'home'">
          <v-icon>mdi-home</v-icon>
        </v-btn>
        <v-btn icon @click="dis = 'contact'">
          <v-icon>mdi-email</v-icon>
        </v-btn>
        <v-btn icon  @click="dis = 'projects'">
          <v-icon>mdi-information</v-icon>
        </v-btn>
      </v-app-bar>

      <div v-show="dis==='home'">
        <v-row class="align-content-center">
          <v-col>
            <br>
            <h2 id="tldr">TL;DR</h2>
            <br>
            <h3 id="intro">I am a Student at Waukesha County Technical College Studying Web and Software Development and just started Cybersecurity</h3>
          </v-col>
          <v-col>
            <v-img class="center mt-16"
                   src="https://media-exp1.licdn.com/dms/image/D4E03AQFGbGv-3I6K4g/profile-displayphoto-shrink_800_800/0/1639025052734?e=1660780800&v=beta&t=Lq07iXgmqgRRNXDrdKY4qxzqUlnq34qec1YAXu2OJKw">
            </v-img>
          </v-col>


        </v-row >
      </div>
      <div v-show="dis ==='contact'">
        <br>
        <h1 id="hello">Contact Information</h1>
      </div>
      <div v-show="dis === 'projects'">
        <br>
        <h1 id="hello">Projects</h1>
        <v-row class="ma-3">
          <v-col lg="4">
            <a class="project-items" href="https://melodydate.netlify.app/#/">
              <v-card elevation="12" class="pa-4">
                <v-img
                    src="https://thumbs.dreamstime.com/b/heart-shape-red-pixel-isolated-white-background-square-clip-art-cute-icon-simple-plain-tile-pattern-concept-love-sign-178857521.jpg"></v-img>
                <h2>Dating Mock App</h2>
                <br>
                <h3>Description</h3>
                <p>A mobile web application based on your Spotify music using:</p>
                <ul>
                  <li>Spotify API</li>
                  <li>Firebase</li>
                  <li>Vue 2</li>
                  <li>Node.js</li>
                </ul>
              </v-card>
            </a>
          </v-col>
          <v-col lg="4" sm="12">
            <a class="project-items" href="https://github.com/JHidalgo24/MovieDatabaseAssignment.git">
              <v-card elevation="12" class="pa-4">
                <v-img
                    src="https://media.istockphoto.com/vectors/movie-time-vector-illustration-cinema-poster-concept-on-red-round-vector-id911590226?k=20&m=911590226&s=612x612&w=0&h=HlJtSKF-fLsKFy1QJ-EVnxXkktBKNS-3jUQPXsSasYs="></v-img>
                <h2>Movie Database Manager</h2>
                <br>
                <h3>Description</h3>
                <p>A console application for managing movies using Databases, Json, and CSV files:</p>
                <ul>
                  <li>C#</li>
                  <li>Entity Framework</li>
                  <li>Nuget</li>
                  <li>CSV and JSON files</li>
                </ul>
              </v-card>
            </a>
          </v-col>
          <v-col lg="4" sm="12">
            <a class="project-items" href="https://github.com/JHidalgo24/PokemonDeckBuilder.git">
              <v-card elevation="12" class="pa-4">
                <v-img
                    src="https://images-na.ssl-images-amazon.com/images/I/71WRDRjaK9L.jpg">
                </v-img>
                <h2>Pokemon Deck Builder</h2>
                <br>
                <h3>Description</h3>
                <p>A deck building & card searching website for Pokemon Cards</p>
                <ul>
                  <li>Firebase</li>
                  <li>APIs</li>
                  <li>Authentication</li>
                  <li>Vue 2 and Node.js</li>
                </ul>
              </v-card>
            </a>
          </v-col>
          <v-col></v-col>
        </v-row>
      </div>

    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {},

  data() {
    return {
      dis: 'home'
    }
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Merriweather+Sans:wght@300&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Koulen&display=swap');

* {
  font-family: 'Merriweather Sans', sans-serif;
  color: black;
}

.center {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 90%;
}

#hello {
  padding-left: 20px;
  font-family: 'Koulen', cursive;
  font-size: 60px;
  color: orangered;
  font-weight: bold;
  border-radius: 0px 40px 0px 40px;
}

#intro {
  padding-left: 20px;
  font-size: 40px;
  color: black;
}

.project-items {
  text-underline: none;
  color: black;
  text-decoration: none;
}
#tldr{
  padding-left: 20px;
  font-family: 'Koulen', cursive;
  font-size: 55px;
  color: darkslateblue;
  font-weight: bold;
}


</style>
