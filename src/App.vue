<template>
  <div id="app">
    <h1>Welcome to App</h1>
      <UserProfile/>
      <Img/>
  </div>
</template>

<script>
import UserProfile from './components/UserProfile'
import Img from './components/Img'

export default {
  name: 'App',
  components: { UserProfile, Img}

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f3f5f6;
  background:rgba(0, 0, 0, 0.637);
  width: 100%;
  height: 100%;
}

h1 {
  padding-top: 20px;
}

</style>