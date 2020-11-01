<template>
  <div id="app">
    <h1>Welcome to App</h1>
      <UserProfile/>
  </div>
</template>

<script>
import UserProfile from './components/UserProfile'

export default {
  name: 'App',
  components: { UserProfile }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f3f5f6;
  margin-top: 60px;
  background:rgba(46, 139, 86, 0.562);
  border-radius: 15px;
}



</style>