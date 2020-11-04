<template>
    <h1>{{ logotype }}</h1>
    <nav class="menu">
        <ul>
            <template v-for="list in lists" :key="list">
                <li>
                    <a href="#">{{list}}</a>
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
           logotype: '',
           lists: ['Home', 'About', 'Services', 'Projects'],
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