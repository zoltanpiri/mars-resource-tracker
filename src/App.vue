<template>
  <title-component/>
  <resources-component/>
</template>

<script>

import TitleComponent from "@/components/Title";
import ResourcesComponent from "@/components/Resources";

export default {
  name: 'App',
  components: {
    ResourcesComponent,
    TitleComponent  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
