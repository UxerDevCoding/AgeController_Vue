<template>
  <v-footer padless>
    <v-col class="text-center" cols="12">
      {{ new Date().getFullYear() }} — <strong>Omar Hevia</strong>
    </v-col>
  </v-footer>
</template>

<script>
export default {
  name: "FooterBar",
  data: () => ({}),
};
</script>

<style scoped>
.theme--light.v-sheet {
  background-color: rgba(59, 212, 212);
  border-color: #4caac7;
  color: #252424ec;
}

.text-center {
  font-family: "Lucida Sans";
}
</style>
