<template>
  <div id="app">
    @{{user.username}} - {{fullName}}
    <strong>Followers: </strong> {{followers}}
    <button v-on:click="followUsers">Follow</button>
  </div>
</template>

<script>


export default {
  name: 'App',

  data(){
    return {
      followers: 0,
      user: {
        id: 1,
        username: '_AlongeNet',
        firstName: 'Alexsey',
        lastName: 'Gusakov',
        email: 'alongenet32@gmail.com',
        isAdmin: true,
      },
    }
  },

  watch: {
    followers(newFollowerCount, oldFollowerCount){
      if(oldFollowerCount < newFollowerCount){
        console.log(`${this.user.username} has gained a follower`);
      }
    }
  },
  computed: {
    fullName(){
      return `${this.user.firstName} ${this.user.lastName}`;
    }
  },
  methods: {
    followUsers(){
      this.followers++;
    }
  },

  mounted(){
    this.followUsers();
  }
    
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
button{
  width: 6rem;
  height: 2rem;
  border-radius: 40px;
  color:#f2f4f7;
  background: #084936;
  outline:none;
}
</style>
