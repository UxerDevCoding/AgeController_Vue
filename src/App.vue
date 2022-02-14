<template>
  <v-app>
    <v-main>
      <router-view />
    </v-main>
    <footer-bar />
  </v-app>
</template>

<script>
import FooterBar from "./components/FooterBar.vue";

export default {
  name: "App",

  data: () => ({
    //
  }),
  components: {
    FooterBar,
  },
};
</script>
