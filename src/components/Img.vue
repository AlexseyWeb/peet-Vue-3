<template>

  <div class="images" >
     <img v-for="img in images" :src="img" :key="img.title"/>
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
       'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSasFktSE91eckIqEnG5XDAeE61AC_xE-ENgw&usqp=CAU',
       'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSiuIgsfiWIOUBEaLqnji7DohZIWLrXzzh2dA&usqp=CAU',
       'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTDxhKKcVzSWx8FrpxcmMZQW2Zi24XYDYXntQ&usqp=CAU',
       
       ]
      } 
        
   },
    
  
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
        transition: all 4s ease-in;
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
        
    }

</style>>

