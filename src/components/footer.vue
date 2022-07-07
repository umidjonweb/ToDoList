<template>
  <div class="container"  v-if="comments.length > 0">
    
     <h3 class="text-center text-primary">comentiya mavjud</h3>
     <div class="comment" v-for="comment in comments" :key='comment.id'  >
        <div>
           <p>ism: <b>{{comment.name}}</b> </p>
        </div>
        <div>
           <button class="btn btn-primary"  @click="$emit('remove',comment)" >delete</button>
        </div>
     </div>

  </div>
  <div v-else>
      <h3 class="text-center text-danger" >comentiya mavjud emas</h3>
  </div> 
</template>

<script>
 
export default {
   props:{
     comments:{
        type:Array,
        required:true
     }
   },
   methods: {
   
   },

}

</script>

<style>
.comment{
   display: flex;
   justify-content: space-between;
   border: 3px solid blueviolet;
   align-items: center;
   padding: 20px;
   margin: 20px;
}
</style>