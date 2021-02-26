<template>
  <div id="app">
    <NavBar :logged="true" :account="Ichii" />
    <router-view/>
  </div>
</template>

<style lang="scss">
  body {
    margin: 0;
  }
</style>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import NavBar from '@/components/NavBar.vue'; // @ is an alias to /src

@Component({
  components: {
    NavBar,
  },
})
export default class Home extends Vue {}
</script>