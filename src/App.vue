<template>
  <app-layout></app-layout>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'
import AppLayout from './views/AppLayout.vue'

@Component({
  components: {
  AppLayout,
  },
  })
export default class App extends Vue {
}
</script>
