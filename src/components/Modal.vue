<template>
  <div class="modal" v-if="show" @click.stop="hideModal()" >
    <div @click.stop class="modal_content">
      <header/>
    </div>
  </div>
</template>

<script>

export default {
   name:"Modal",
   components:{
    
   },
props:{
   show:{
      type:Boolean,
      default:false
   }
},
methods: {
   hideModal(){
      this.$emit('update:show',false);
   

   }
},
}
</script>

<style scoped>
.modal{
   position: fixed;
   top: 0;
   bottom: 0;
   left: 0;
   right: 0;
   z-index: 10;
   display: flex;
   background-color: rgba(0,0,0,.5);
}
.modal_content{
   margin: auto;
   background-color: white;
   width: 50%;
   min-height: 120px;
   padding: 20px;
}
</style>