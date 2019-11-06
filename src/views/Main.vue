<template id="main">
  <v-ons-page>
  <v-ons-splitter>
    <v-ons-splitter-side
      swipeable width="150px" collapse="" side="left"
      :open.sync="openSide"
    >
      <v-ons-page>
        <v-ons-list>
          <v-ons-list-item v-for="page in pages"
            tappable modifier="chevron"
            @click="currentPage = page; openSide = false"
          >
            <div class="center">{{ page }}</div>
          </v-ons-list-item>
        </v-ons-list>
      </v-ons-page>
    </v-ons-splitter-side>

    <v-ons-splitter-content>
      <component :is="currentPage" :toggle-menu="() => openSide = !openSide"></component>
    </v-ons-splitter-content>
  </v-ons-splitter>
  </v-ons-page>
</template>

<script>
import Home from "@/components/Home";

export default {
  name: 'main',
  data() {
    return {
      currentPage: 'Home',
      pages: ['Home'],
      openSide: false
    };
  },
  components: {
    Home
  },
  components: {
    
  }
}
</script>

<style lang="scss">
</style>