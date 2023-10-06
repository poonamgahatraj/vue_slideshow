<template>
  <div class="container">
    <img :src= "imageList[currentindex]">
<div  class="btn">
  <button @click="prev">Previous</button>
  <button @click="next">Next</button>
</div>
  </div>
 

</template>

<script >
export default{
    data(){

        return{
          imageList:[
            
          "public/assets/img_mountains_wide.jpg",
          "public/assets/img1.jpg",
          "public/assets/img2.jpg",
          "public/assets/img3.jpg"
        
        ],
        currentindex:0,
        current_location:""
        
        }
    },

    methods:{
      
     
      prev(){
         
                  

                  console.log("hellotest")
                  if (this.currentindex<=0)
              {
                  
                  this.currentindex=this.imageList.length-1
                  
              }

              if (this.currentindex>0)
              {
                  this.currentindex=this.currentindex-1;
              }
            

                current_location=this.imageList[currentindex];
      },


      

      next(){
        console.log("next")
       
    if ( this.currentindex>this.imageList.length)
    {
        this.currentindex=this.imageList[0]
        
    }

    if(this.currentindex<this.imageList.length)
    {
        this.currentindex++;
    }

   

         current_location=this.imageList[currentindex];

      }
      
    }

  }
   

</script>

<style scoped>
.container{
  
  display: flex;
    flex-direction: column;
    justify-content: center;
}

.btn{
  display: flex;
    justify-content: space-between;
}
</style>