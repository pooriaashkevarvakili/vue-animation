<template>
  <div class="text-primary py-4 text-center" style="border:1px solid #000">
    <transition name="button" mode="in-out">
    <button v-if="!showButton" class="btn btn-primary" @click.prevent="onShowButton()">
      off
    </button>
    <button v-else class="btn btn-primary" @click.prevent="onShowButton()">on
    </button>
    </transition>
  </div>
</template>

<script>
export default {
  data(){
    return{
      showButton:true
    }
  },
  methods:{
    onShowButton(){
      this.showButton=!this.showButton
    }
  }
}
</script>

<style scoped>
.button-enter-from,.button-leave-to{
  opacity:0;
transform: translateX(-30px);
}
.button-enter-to,
.button-leave-from
{
  opacity:1;
  transform: translateX(-30px);
}
.button-enter-active,.button-leave-active{
transition: all 1s;
}
</style>
