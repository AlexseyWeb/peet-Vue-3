<template>
    <div class="form">
        <input  type="text" v-model="message" class="msg" placeholder="reactive add text in paragraph">
        <p>{{message}}</p>
    </div>
     
</template>



<script>

export default {
    name: 'FormMenu',
    data(){
        return {
            message: ''
        }
    }

    
}

</script>



<style scoped>
.form {
    margin-top: 50px;
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
}



input[type='text']:focus{
    border: none;
    outline: none;
}
</style>