<template>
    <div class="second-menu">
        <button class="gamburger"  v-on:click="showMenu"><i class="fas fa-bars"></i></button>
        <div class="menu-panel" v-show="!show">
            <ul class="list">
                <template v-for="item in menuItem" :key="item">
                    <li class="list-item"><a href="#">{{item}}</a></li>
                </template>
            </ul>
        </div>
    </div>
</template>





<script>


export default {
        
    data(){
        return {
            show: true,
            
            menuItem: ['Profile', 'Recomendations', 'Job'],

        }
    },

    methods: {
        showMenu(){
            this.show = !this.show;
        }
    },

    computed: {

    }

}
</script>



<style scoped>
    .gamburger {
        width: 100px;
        height: 50px;
        background: none;
        border: none;
        outline: none;
    }

.gamburger > i{
    font-size: 40px;
    color: rgb(169, 36, 192);
    background: none;
    position: absolute;
    right: 10px;
}

    .menu-panel{
        position: absolute;
        top: 10px;
        left: 0;
        bottom: 0;
        background: rgba(75, 3, 3, 0.794);
        width: 30vw;
        display: flex;
        align-items: center;
        flex-direction: column;
       box-shadow: 6px 6px 6px  white;
        border-radius: 10px;
    }

    .list {
        list-style-type: none;
        margin: 0;
        padding: 0;
    }
    .list-item {
        margin: 0;
        padding: 0;
        cursor: pointer;
    }
    .list-item >a {
        text-decoration: none;
        font-size: 24px;
        color: white;

    }
    .list-item >a:hover{
        color:teal;
    }

</style>