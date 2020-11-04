<template>
    <h1>{{ logotype}}{{show()}}</h1>
    <nav class="menu">
        <ul>
            <template v-for="list in lists" :key="list">
                <li>
                    <a href="#" :title="list">{{ list }}</a>
                </li>
            </template>
        </ul>
    </nav>
</template>



<script>
export default {
    name: 'Navigator Menu',
    data () {
       return {
           username: {
               firstName: 'Alexsey',
                lastName:  'Gusakov'
           },
           logotype: '',
           lists: ['Home', 'About', 'Services', 'Projects'],
       } 
    },

    methods: {
     
           show() {
               console.log(`all data on component ${JSON.stringify(this.username)} ${this.logotype} ${JSON.stringify(this.lists)}`);
           }
        
    }
}
</script>


<style scoped>
h1 {
    font-size: 24px;
    color:chocolate;
    text-align: left;
    padding-left: 20px;
}

nav{
    display: flex;
    justify-content: center;
    align-items: center;
}
ul {
    list-style: none;
    display: flex;
    justify-content: center;
}
li {
    padding: 0;
    margin: 0;
    justify-content: center;
    cursor: pointer;
}
li>a {
    color:darkred;
    font-size: 24px;
    text-decoration: none;
    margin-left: 20px;
}
li > a:hover{
    color:white;
    transition: color 1s ease-in;
}


</style>