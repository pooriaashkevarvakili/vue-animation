<template>
  <div class="text-center">
    <transition>
    <p v-if="showParagraph">Hai leela</p>
    </transition>
    <button class="btn btn-primary" @click.prevent="onToggle() ">toggle The Text</button>
  </div>
</template>

<script>
export default {
  name: "TheParagraph",
  data(){
    return{
showParagraph:true
    }
  },
  methods:{
    onToggle(){
this.showParagraph=!this.showParagraph
    }
  }
}
</script>

<style src='./../style/style.css' >

</style>
