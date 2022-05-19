<template>
  <v-app>
    <v-main>
      <v-app-bar class="pa-3" color="white" elevation="0">
        <h2 style=" text-align: left"> Justin Hidalgo</h2>
        <v-spacer></v-spacer>
        <v-btn text @click="dis = 'home'">
          Home
          <v-icon>mdi-home</v-icon>
        </v-btn>
        <v-btn text  @click="dis = 'contact'">
          Contact
          <v-icon>mdi-email</v-icon>
        </v-btn>
        <v-btn text  @click="dis = 'projects'">
          Projects
          <v-icon >mdi-information</v-icon>
        </v-btn>
      </v-app-bar>

      <div v-show="dis==='home'">
        <v-row class="align-content-center">
          <v-col >
            <h1 id="hello">Hello!</h1>
            <h2 id="intro">I'm Justin,<br>
  A Software and Web Developer based in Wisconsin </h2>
          </v-col>
          <v-col>
            <v-img class="center mt-16"
                   src="https://t1.ea.ltmcdn.com/en/posts/6/8/9/happy_dog_names_male_and_female_2986_600_square.jpg">
            </v-img>
          </v-col>


        </v-row>
      </div>
      <div v-show="dis ==='contact'">
        <h1 id="hello" >Contact Information</h1>
      </div>
      <div v-show="dis === 'projects'">
        <h1 id="hello" >Projects</h1>
      </div>

    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {},

  data(){
    return{
        dis:'home'
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
  font-size: 90px;
  color: darkorange;
  font-weight: bold;
  border-radius: 0px 40px 0px 40px;
}
#intro{
  padding-left: 20px;
  font-size: 40px;
}



</style>
