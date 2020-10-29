<template>
    <div class="user-profile">
        <div class="user-profile__user-panel">
            <h1 class="user-profile__username">@{{ user.username }}</h1>
            <div class="user-profile__admin-badge" v-if="user.isAdmin">
                Admin
            </div>
            <div class="user-profile__follower-count">
                <strong>Followers:</strong> {{ followers }}
            </div>
        </div>
        <div class="user-profile__list-jobs">
            <div class="user-profile__job" v-for="job in user.listOfJobs" :key="job.id">
                {{ job.job }}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "UserProfile",
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
        listOfJobs: [
            {id:1, job:'Frontend'},
            {id: 2, job:'Backend'}
        ],
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


<style scoped>

.user-profile{
    display: grid;
    grid-template-columns: 1fr 3fr;
    width: 100%;
    padding: 50px 5%;
}

.user-profile__user-panel{
    display: flex;
    flex-direction: column;
    margin-right: 50px;
    padding: 20px;
    background-color: white;
    border-radius: 5px;
    border: 1px solid #DFE3E8;
}

.user-profile__admin-badge {
    color: white;
    border-radius: 5px;
    background:rebeccapurple;
    font-weight: bold;
    margin: 0 auto;

}

h1 {
    margin: 0;
}



</style>