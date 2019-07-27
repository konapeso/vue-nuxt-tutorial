<template>
  <div class="hello">
    <h1>{{title}}</h1>
    <p>{{message}}</p>
    <hr/>
    <button v-on:click="doAction">
      Show/Hide
    </button>
    <br><br>
    <transition name="transit">
      
    <p v-if="flg" class="trans">Transition!</p>
      
    </transition>
  </div>
</template>




<script>
export default {
  name: 'Hello World',
  props:{
    title:String,
  },
  data: function(){
    return{
      message:'Transition Sample!',
      flg: true,
      btn: 'Hide', 
    };
  },
  methods:{
    doAction:function(){
      this.flg = !this.flg;
    },
    
  },
  
  


}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>


.trans{
  width: 150px;
  background-color: #ddf;
  padding:10px;
  font-size:20pt;
}

.transit-leave-active{
  animation: anim 5.0s;
}
.transit-enter-active{
  animation: anim 2.5s reverse;
}

@keyframes anim {
  0%{
    tranceform: translateX(0px) trancelateY(0px) rotateZ(0deg);
    opacity:1.0;
    background-color: #ddf;
  }
  25%{
    transform: translateX(250px) translateY(0px) rotateZ(0deg);
    opacity:1.0;
    background-color: #fdd;
  }
  50%{
    transform: translateX(0px) translateY(-100px) rotateZ(540deg);
    opacity: 1.0;
    back-ground-color: #fdf;

  }
  100%{
    transform: translateX(0px) translateY(-200px) rotateZ(1080deg);
    opacity:0;
    background-color: #ffd;
  }
}

</style>
