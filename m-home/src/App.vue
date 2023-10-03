<template>
 <div id="app">
  <Navigation />
  <RouterView />
 </div>
</template>

<script>
import { RouterLink, RouterView } from 'vue-router'
import Navigation from './components/Navigation.vue';

export default {
  components: {
    Navigation
  },
  methods:{

  },
  
}
</script>

<style lang="scss" scoped></style>


