<template>
  <div id="app">
    <h1>Welcome to the photo gallery</h1>
    <Nav>
      <NavItem/>
    </Nav>
      <imgCard/>
  </div>
</template>

<script>

import imgCard from './components/Img';
import Nav from './components/Navigation';
import NavItem from './components/NavItem';

export default {
  name: 'App',
  components: { Nav, NavItem, imgCard},
 

}
</script>

<style scoped>
#app {
  
  font-family: 'ROBOTO', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f3f5f6;
  background:rgba(0, 0, 0, 0.637);
  width: 100%;
  height: 100%;
  
}

h1 {
  margin-top: 20px;
  margin-bottom: 20px;
  text-align: center;
}

</style>