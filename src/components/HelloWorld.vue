<template>
  <v-app>
    <v-app-bar color="primary" app>
      <v-toolbar-title>Vuetify Training</v-toolbar-title>
      <v-btn text rounded>Home</v-btn>
      <v-btn text rounded>Login</v-btn>
    </v-app-bar>
    <v-main>
      <v-card width="400" class="mx-auto mt-5">
        <v-card-title>
          <h1 class="display-1">Login Page</h1>
        </v-card-title>
        <v-card-text>
          <v-text-field prepend-icon="mdi-account-circle" label="Username"></v-text-field>
          <v-text-field prepend-icon="mdi-lock" @click:append="showPassword=!showPassword" :append-icon="showPassword?'mdi-eye-off':'mdi-eye'" :type="showPassword?'password':'text'" label="Password"></v-text-field>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions>
          <v-btn color="success">Register</v-btn>
          <v-spacer></v-spacer>
          <v-btn color="info">Login</v-btn>
        </v-card-actions>
      </v-card>
    </v-main>
    <v-spacer></v-spacer>
    <v-footer app class="bg-green-lighten-1" dark>
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
        {{ new Date().getFullYear() }} — <strong>Vuetify Training</strong>
      </v-col>
    </v-row>
  </v-footer>
  </v-app>
</template>


<script>

export default {
  name: 'HelloWorld',

  data: () => ({
    showPassword:false,
    links:['Home','About Us','Team','Services','Blog','Contact Us']
  })
}
</script>
