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
            <form class="user-profile__create-list">
              <label for="newList"><strong>New List</strong></label>
              <textarea id="newList" rows="4"></textarea>
            </form>

            <div class="user-profile__create-list-type">
              <label for="newListType"><strong>Type: </strong></label>
              <select id="newTwoType">
                <option :value="option.value" v-for="(option, index) in listTypes" :key="index">
                  {{ option.name }}
                </option>
              </select>
            </div>
        </div>
        <div class="user-profile__list-jobs">
            <ListItem
             v-for="list in user.listOfJobs" 
             :key="list.id" 
             :username="user.username" 
             :list="list"
             @favorite="toggleFavorite"/>
        </div>
    </div>
</template>

<script>
import ListItem from './ListItem'

export default {
    name: "UserProfile",
    components:{ ListItem },
     data(){
    return {
      listTypes: [
        {value: 'open', name: 'Open '},
        {value: 'edit', name: 'Editor'}
      ],
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
    },
    toggleFavorite(id) {
      console.log(`Favorite Tweet ${id}`);
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
    grid-template-columns: 1fr 2fr;
    width: 50%;
    padding: 50px 5%;
}

.user-profile__user-panel{
    display: flex;
    flex-direction: column;
    margin-right: 50px;
    padding: 20px;
    background-color: rgba(0, 0, 0, 0.431);
    border-radius: 5px;
    border: 1px solid #DFE3E8;
}

.user-profile__admin-badge {
    color: rgb(129, 6, 88);
    border-radius: 5px;
    background:rgba(88, 25, 5, 0.424);
    font-weight: bold;
    margin: 0 auto;

}

.user-profile__create-list {
  display:flex;
  flex-direction: column;
  border-top: 1px solid black;
  padding-top: 20px;
}
    
h1 {
    margin: 0;
}

user-profile__list-jobs {
  display: flex;
  justify-content: center;
  height: 400px;
  width: 400px;
}


</style>