<template>
  <div>
  <div id="app">

    <div class='tata'>
      <div :style='vrednost'  class='sincic'>
        <div :style='kontraVrednost' class='sinovSin'></div>
      </div>
    </div>


    </div>
    <div style='margin-left:1000px;'>
      <button @click='uvecajDesno'>rokaj desno</button>
      <button @click='uvecajDole'>rokaj dole</button>
  </div>
</div>
</template>

<script>

export default {
  name: 'app',
  data(){
    return{
      desno:0,
      dole:0
    }
  },
  methods:{
    uvecajDesno: function(){
      this.desno+=100;
    },
    uvecajDole: function(){
      this.dole+=100;
    }
  },

  computed:{
 vrednost: function(){
    return 'margin-left: '+ this.desno +'px; margin-top: '+ this.dole+'px;';

  },
  kontraVrednost: function(){
     return 'margin-left: '+ (0-this.desno) +'px; margin-top: '+ (0-this.dole)+'px;';

   }
  }


}
</script>

<style>
  body{
    background-image: url('./assets/slika.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
    margin: 0;
    padding: 0;
  }
  .tata{
    position: fixed;
    width: 800px;
    height: 900px;
    background-color: red;
  }
  .sincic{
    transition: 3s;
    margin-left: 1px;
    width: 150px;
    height: 150px;
    overflow: hidden;


  }
  .sinovSin {
    transition: 3s;
    margin-left: 1px;
    width: 1900px;
    height: 900px;
    background-image: url('./assets/slika.jpg');
    background-repeat: no-repeat;
    background-size: cover;

  }
  /*.mama{
    margin-left: 500px;
    z-index: 1;
    position: relative;
    width: 100px;
    height: 100px;
    background: inherit;

  }
  .mama::before {
    content: '';
    position: absolute;
    z-index: -1;


  }
  .mama::after {
    content: '';
    position: absolute;
    z-index: -1;
    background-color: blue;
  }*/
</style>
