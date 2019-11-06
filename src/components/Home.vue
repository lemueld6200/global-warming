<template id="home">
  <v-ons-page>
    <Toolbar title="Home" :action="toggleMenu" />
    <p style="text-align: center">
      Welcome home.
    </p>
  </v-ons-page>
</template>

<script>
import Toolbar from "./Toolbar";

export default {
  name: "home",
  components: {
    Toolbar
  }
}
</script>