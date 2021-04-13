<template>
<div>
  <transition name="backdrop">
 <div class="backdrop" v-if="open">

 </div>
  </transition>
  <transition>
  <div class="dialog" v-if="open">

<slot>

</slot>

  </div>
  </transition>
</div>
</template>

<script>
export default {
  props:['open'],
  name: "DialogModal",

}
</script>

<style scoped>
.backdrop{
  background: rgba(0,0,0,0.5) ;
  position: fixed;
  width:100%;
  height:100%;
  top:0;
  left:0;
}
.dialog{
  top:20%;
  position:fixed;
  background:#fff;
  width:60vw;
  left:20vw;
  padding:20px
}
.v-enter-from{
  transform:translateY(-200px)
}
.v-enter-to{
  transform:translateY(0px)

}
.v-enter-active{
  transition:transform 0.5s
}
.v-leave-from{
  transform:translateY(0px)
}
.v-leave-to{
  transform:translateY(-200px)

}
.v-leave-active{
  transition:transform 0.5s
}
.backdrop-enter-from{
opacity:0
}
.backdrop-enter-to{
opacity:1
}
.backdrop-enter-active{
transition:opacity 1s;
}
</style>
