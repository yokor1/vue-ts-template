<template>
  <v-toolbar absolute clipped-left app class="primary">
    <v-toolbar-side-icon @click="activeDrawerClicked"></v-toolbar-side-icon>
    <v-toolbar-title>Title</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items class="hidden-sm-and-down">
      <v-btn flat>Link One</v-btn>
      <v-btn flat>Link Two</v-btn>
      <v-btn flat>Link Three</v-btn>
    </v-toolbar-items>
  </v-toolbar>
</template>

<script lang="ts">
import { Component, Emit, Vue } from 'vue-property-decorator'

@Component({})
export default class AppToolbar extends Vue {
  @Emit('activeDrawerClicked') activeDrawerClicked () {
    console.log('drawer')
  }
}
</script>

<style scoped>

</style>
