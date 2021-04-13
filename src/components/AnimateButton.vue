<template>
  <div class="text-primary py-4 text-center" style="border:1px solid #000">
<button v-if="!showOnButton" class="btn btn-primary" @click.prevent="onShowButton">
  off
</button>
  <button class="btn btn-primary" @click.prevent="onShowButton">on </button>
  </div>
</template>

<script>
export default {
  data(){
    return{
showOnButton:true
    }
  },
  name: "AnimateButton",
  methods:{
    onShowButton(){
this.showOnButton=!this.showOnButton
    }
  }
}
</script>

<style scoped>

</style>
