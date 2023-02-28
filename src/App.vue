<template>
  <v-app>
    
    <v-app-bar app color ="primary" dark>
      <v-tool-bar-tittle> Vuetify Dashboard</v-tool-bar-tittle>
      <v-spacer></v-spacer>
      <v-btn text rounded>Home</v-btn>
      <v-btn text rounded>Login</v-btn>
    </v-app-bar>
    <v-main>
     <!----Login Module---> 
  <v-card width ="400" class="mx-auto mt-5">
  <v-card-title> 
        <h2 class ="display-1"> Login </h2>
  </v-card-title>

  <v-card-text>
    <v-form>
      <v-text-field 
      label="Username"
      prepend-icon ="mdi-account-circle"/>
      <v-text-field 
      :type ="showPassword ?'text': 'Password'"
      label="Password"
      prepend-icon ="mdi-lock"
      :append-icon = " showPassword ? 'mdi-eye':'mdi-eye-off'"
      @click:append = "showPassword = !showPassword"/>
    </v-form>
  </v-card-text>
  <v-divider></v-divider>
  <v-card-actions>

    <v-btn color ="success">Register</v-btn>
    <v-spacer></v-spacer>
    <v-btn color ="info">Login</v-btn>
  </v-card-actions>
</v-card>
    </v-main>
    
  <v-footer class="bg-grey-lighten-1">
    <v-row justify="center" no-gutters>
      <v-btn
        v-for="link in links"
        :key="link"
        color="white"
        variant="text"
        class="mx-2"
        rounded="xl"
      >
        {{ link }}
      </v-btn>
      <v-col class="text-center mt-4" cols="12">
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-col>
    </v-row>
  </v-footer>

  </v-app>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',

  components: {
    
  },

  data: () => ({
    showPassword : false,
    links:[
      'Home',
      'Login'
    ]
  }),
  
}
</script>
