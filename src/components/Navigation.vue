<template>
    <button v-on:click="addItemMenu">addItemMenu</button>
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
           logotype: 'Click Me',
           lists: ['Home', 'About', 'Services', 'Projects'],
       } 
    },

    methods: {
     
           show() {
               console.log(`all data on component ${JSON.stringify(this.username)} ${this.logotype} ${JSON.stringify(this.lists)}`);
           },
           showWelcome(str){
               alert(str);
           },
            xLogoType() {
                return this.logotype = 'Level up!';
            },
            addItemMenu(){
                this.lists.push('WO!');
            },
            changeName(){
                return this.username.firstName = 'Guest';
            },
            changeLastName(){
                return this.username.lastName = 'Undefined';
            },
            changeUser(){
                this.changeName();
                this.changeLastName();
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
    flex-wrap: wrap;
}
ul {
    list-style: none;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
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
    transition: color .5s ease-in;
}

button {
	box-shadow:inset 0px 1px 0px 0px #f29c93;
	background:linear-gradient(to bottom, #fe1a00 5%, #ce0100 100%);
	background-color:#fe1a00;
	border-radius:22px;
	border:1px solid #d83526;
	display:inline-block;
	cursor:pointer;
	color:#070707;
	font-family:Arial;
	font-size:15px;
	font-weight:bold;
	padding:6px 24px;
	text-decoration:none;
	text-shadow:0px 1px 0px #b23e35;
    outline: none;
}
button:hover {
	background:linear-gradient(to bottom, #ce0100 5%, #fe1a00 100%);
	background-color:#ce0100;
}
button:active {
	position:relative;
	top:1px;
    
}

.welcome {
    margin-left: 40px;
}

</style>