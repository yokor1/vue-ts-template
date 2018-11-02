<template>
  <v-app>
    <app-toolbar @activeDrawerClicked="activeDrawer"></app-toolbar>
    <app-drawer v-bind:drawer='fuck'></app-drawer>
    <v-content>
      <v-container fluid>
        <router-view></router-view>
      </v-container>
    </v-content>
    <v-footer class="primary" app></v-footer>
  </v-app>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'
import AppDrawer from '../components/AppDrawer'
import AppToolbar from '../components/AppToolbar'

@Component({
  components: {
  AppDrawer,
  AppToolbar,
  },
  })
export default class AppLayout extends Vue {
  fuck: boolean;
  activeDrawer () {
    this.fuck = true
    console.log('active drawer')
  }
}
</script>
<style scoped>

</style>
