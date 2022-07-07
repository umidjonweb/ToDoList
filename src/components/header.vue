<template>
  <div class="header w-50 mx-auto">
   <input type="text" placeholder="ismni kiriting" class="form-control w-100 my-3" v-model="comment.name"  >
   <button class="btn btn-primary"  @click="xodisa">Add comment</button>
  </div>
  </template>  
<script>
export default {
   name:'header',
data() {
   return {
     comment:{
        name:''
     }
   };
},
methods: {
   xodisa(){
      this.comment.id=Date.now();
      this.$emit('addcom',this.comment);
      this.comment={
         name:'',
      }
   }
},
}
</script>

<style>

</style>