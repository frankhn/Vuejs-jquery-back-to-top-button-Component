<template>
  <div id="app">
    <link rel="stylesheet"
	href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <router-view/>
    <BackTopFromScratch />
  </div>
</template>

<script>
import BackTopFromScratch from '@/components/BackTopFromScratch'
export default {
  name: 'App',
  components: {
    BackTopFromScratch
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
