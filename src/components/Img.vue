<template>

  <div class="images" >
     <img v-for="(img, index) in images" :src="img" :key="img"  v-on:click="removeImg(index)" loading="lazy"/>
  </div>

</template>



<script>

export default {
    
   data() {
      return {
       images :['https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSKTrAGfLGPNDfT0fKyKlSxvPwdRjy7JHbLtg&usqp=CAU',
       'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTfRHH3uwBsPV-Z5yPXWtc2EHWzgD7FrsjflQ&usqp=CAU',
       'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTQHsuzlmRErb-IgWk5Jo-37MAjQQbww2J7Xw&usqp=CAU',
       'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQ0ybMdc-AjM05QOZd1y_xlGuCceyJPnaZm6g&usqp=CAU',
       
       ]
      } 
        
   },
    methods: {
      removeImg(index){
        this.images.splice(index, 1);
      }
    }
  
}

</script>


<style scoped>

.images {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
}
    img{
        margin-top:40px;
        width: 20%;
        height: 30%;
        transition: all 5s ease-in;
        border-radius: 40px;
        box-shadow: 6px 6px 6px rgba(161, 6, 6, 0.774);
        margin-left: 60px;
        border: 4px solid rgba(161, 6, 6, 0.7);
        justify-content: center;
        align-items: center;
        
        
        
    }
    img:hover{
        transform: skew(35deg, 20deg);
        transform: scaleZ(3deg);
      transition: border 2.3s 0s ease;
    }

</style>>

