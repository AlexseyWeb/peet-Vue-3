<template>
    <div class="form">
        <input  type="text" v-model="message" v-on:keyup.enter="addItem" class="msg" placeholder="reactive in Vue add text in paragraph and  press key Enter">
        <ul>
            <li class="list-on-input" v-for="(item, index) in items" :key="item.id" v-on:click="removeItem(index)">
              <input type="checkbox" v-model="checked" > {{index + 1 }} {{  item }}
            </li>
        </ul>
    </div>
     
</template>



<script>

export default {
    name: 'FormMenu',
    data(){
        return {
            checked: true,
            message: ' ',
            items: ['Limon', 'Yellow'],
        }
    },

    methods: {
        addItem(){
            this.items.push(this.message);
            this.message = '';
        },
        removeItem(index){
            this.items.splice(index, 1);
        }
    }
    
}

</script>



<style scoped>
.form {
    background: rgb(12, 12, 12);
    height: 400px;
    color: red;
    background: transparent;
    border: none;
    outline: none;
}

.form p {
    font-size: 20px;
}

input[type='text']{
    background: transparent;
    height: 100px;
    font-size: 18px;
    width: 60vw;
    border-radius: 20px;
    caret-color: white;
    color:white;
}

input[type='text']::placeholder{
    text-align: center;
    color: white;
}



input[type='text']:focus{
    border: none;
    outline: none;
}

.list-on-input {
    font-size: 18px;
}
.list-on-input:hover{
    text-decoration: line-through;
}
</style>