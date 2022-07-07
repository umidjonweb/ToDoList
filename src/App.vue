<template>
<navbar :showModal="showModal" />
<div>
   <modal v-model:show="modalVisible">
   
   </modal>
<headers />
<footers :comments="comments" @remove="removeComment"/>
</div>
</template>          
<script>
import footers from './components/footer.vue'
import navbar from './components/Navbar.vue'
import modal from './components/Modal.vue'
import headers from './components/header.vue'
export default {
  components: { 
    footers,
    navbar,
    modal,
    headers,
  },
  data() {
     return {
        comments:[],
        modalVisible:false
     }
     },
     methods: {
        xodisa (comment){
this.comments.push(comment)
this.modalVisible=false;   
        },
        removeComment(izzatillo){  
        console.log(izzatillo)
        this.comments=this.comments.filter(c=> c.id !== izzatillo.id)
        console.log(this.input.value)

        },
        showModal(){
this.modalVisible=true;
        }
     }
  
   
}
</script>

<style lang="scss">

</style>
