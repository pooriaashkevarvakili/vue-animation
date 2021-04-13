<template>
<div class="container">
  <div class="row">
    <div class="col-md-6">
      <div class="box" :class="{animate:animate}"></div>
      <div class="my-3">
        <button class="btn btn-primary" @click.prevent="onAnimateClick()">click me</button>
      </div>
      <div class="my-3">
<TheParagraph/>
      </div>
      <div class="my-3">
        <AnimateParagraph/>
      </div>
      <div class="my-3">

        <dialog-modal :open="openDialog">
          <div>
            this is dialog modal
          </div>
          <div>
            <button class="btn btn-primary" @click.prevent="openDialog=false">okay</button>
          </div>
        </dialog-modal>
        <div class="my-3">
<animate-button>

</animate-button>
          </div>
        <div class="col-md-6">
          <div class="my-3">
          <transition-events>

          </transition-events>
            </div>
        </div>
        <div>
          <button @click.prevent="onopenDialog()" class="btn btn-primary">dialog modal</button> </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
import TheParagraph from "./TheParagraph"
import AnimateParagraph from "./AnimateParagraph"
import DialogModal from "./DialogModal"
import AnimateButton from "./AnimateButton"
import TransitionEvents from "./TransitionEvents";
export default {
  name: 'HelloWorld',
  components:{
    TheParagraph,
    AnimateParagraph,
    DialogModal,
    TransitionEvents,
    AnimateButton
  },
  data(){
return{
animate:false,
  openDialog:false
}
  },
  methods:{
    onAnimateClick(){
this.animate = true
    },
    onopenDialog(){
this.openDialog=true
    }
  },


}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src="./../style/style.css">


</style>
<style>
.v-enter-from{
  transform:translateY(-200px)
}
.v-enter-to{
  transform:translateY(0px)

}
.v-enter-active{
  transition:transform 0.5s
}
</style>
