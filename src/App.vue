<template>
  <div id="app">
    <img src="./assets/logo.png">
    <firestoreInput/>
    <firestoreDisplay/>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld'
import firestoreInput from '@/components/firestoreInput'
import firestoreDisplay from '@/components/firestoreDisplay'
export default {
  name: 'App',
  components: {
    'HelloWorld': HelloWorld,
    'firestoreInput': firestoreInput,
    'firestoreDisplay': firestoreDisplay
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
