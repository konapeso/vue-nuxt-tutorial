<template>
  <div class="hello">
    <h1>{{ title }}</h1>
    <pre>{{ message }}</pre>
    <hr>
    <ol>
     <slot/>
    </ol>
    
    <hr>
    <slot />
    
    
    
  </div>
</template>

<script>
export default {
  name: 'Hello World',
  props: {
    title: String,
  },
  data: function(){
    return{
      message: 'This is message.',
      
    };
  },
  
  


}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
div{
  margin:0px;
  padding:0px;
  text-align:left;
}
h1{
  font-size:72pt;
  font-weight:bold;
  text-align:right;
  letter-spacing:-8px;
  color:#f0f0f0;
  margin:0px;

}
p{
  maegin:0px;
  color:#666;
  font-size:16pt;
}

pre{
  font-size:14pt;
  line-height: 1.25;
}


.area{
  width:300px;
  height:100px;
  background-color:#ddd;
  padding:10px;
  font-size:20pt;
}

.inner{
  color:red;
  font-size:14pt;
}
.etc{
  color:green;
  background-color: #eee;
  font-size:12pt;
  padding:5px;
}

</style>
