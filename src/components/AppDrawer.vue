<template>
  <v-navigation-drawer
    v-model="drawer"
    fixed
    clipped
    class="grey lighten-4" app>
    <v-divider></v-divider>
    <v-list dense class="pt-0">
      <v-list-tile
        v-for="item in items"
        :key="item.title"
      @click="1">
        <v-list-tile-action>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-tile-action>
        <v-list-tile-content>
          <v-list-tile-title>{{ item.title }}</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
    </v-list>
  </v-navigation-drawer>
</template>

<script lang="ts">
import { Component, Prop, Vue, Watch } from 'vue-property-decorator'

@Component({})
export default class AppDrawer extends Vue {
  @Prop({default: true}) drawer: boolean;
  items: Object[];
  right: String | null;
  @Watch('drawer') onDrawerChange () {
    console.log('drawer changed')
  }
  constructor () {
    super()
    this.items = [
      { title: 'Home', icon: 'dashboard' },
      { title: 'About', icon: 'question_answer' }
    ]
    this.right =null
  }
}
</script>

<style scoped>

</style>
