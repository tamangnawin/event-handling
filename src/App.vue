<template>
  <div id="app">
    
    <app-header></app-header>
    <app-events></app-events>
    <app-footer></app-footer>
  </div>
</template>

<script>
import Header from './components/Header';
import Events from './components/Events'
import Footer from './components/Footer';

export default {
  name: 'App',
  components: {
    'app-header': Header,
    'app-events': Events,
    'app-footer': Footer
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
