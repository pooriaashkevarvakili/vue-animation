<template>
<div>
  <transition>
  <p v-if="showParagraph">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus assumenda debitis deserunt dicta dignissimos dolore excepturi ipsa iste minus, necessitatibus odio officia, sed voluptatibus! Doloremque fugiat officiis quaerat qui ut.</p>
  </transition>
</div>
  <div>
    <button class="btn btn-primary" @click.prevent="onToggle()">Toggle</button>
  </div>
</template>

<script>
export default {
  name: "AnimateParagraph",
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

<style scoped >
.v-enter-active{
  animation:animate-para 2s ease-out;
}
.v-leave-active{
  animation:animate-para 2s ease-out;

}
@keyframes animate-para{
  0%{
    opacity: 0;
    transform:translateX(0px)
  }
  25%{
    opacity:0.25;
    transform:translateX(30px)
  }
  50%{
    opacity:50;
    transform:translateX(-30px)
  }
  75%{
    opacity:75;
    transform:translateX(30px)
  }
  100%{
    opacity:1;
    transform:translateX( 0px)
  }
}
</style>
