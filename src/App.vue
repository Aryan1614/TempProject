<template>
  <v-app>
    <div>
      <v-app-bar
        color="deep-purple accent-4"
        dark
      >

        <v-toolbar-title>VIIT Pune</v-toolbar-title>

        <v-spacer></v-spacer>

        <router-link to="/">
          <v-btn style="margin-right: 10px;">
            Home
          </v-btn>
        </router-link>

        <router-link to="/login">
          <v-btn style="margin-right: 10px;">
            Login
          </v-btn>
        </router-link>
      </v-app-bar>
    </div>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  }),
};
</script>
