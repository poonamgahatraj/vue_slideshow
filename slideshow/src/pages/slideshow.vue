<template>
<div v-for="item in imageList" :key="item" class="slideshow-container">
  <img :src="currentImg">

  
  

  
</div>
<div>
  <button @click="prev">Previous</button>
  <button @click="next">Next</button>
</div>

</template>

<script >
export default{
    data(){
        return{
          imageList:["public/assets/img_mountains_wide.jpg",
          "public/assets/img1.jpg",
          "public/assets/img2.jpg",
          "public/assets/img3.jpg"
        
        ],
        currentindex:0
        
        }
    },

    methods:{
      currentImg(){
        imageList[0]
      },

      prev(){
        if (currentindex<=0)
    {
        
        currentindex=imageList.length-1
    }

    if (currentindex>0)
    {
        currentindex=currentindex-1;
    }
  

    imageList[currentindex];
      },


      

      next(){

      }
      
    }

  }
   

</script>