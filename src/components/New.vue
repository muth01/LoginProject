<style>
body{
  background-color:tomato;
}
.message{
  padding-bottom: 20px;
  font-weight: bold;
  }
</style>

<template>

<center>
<table bgcolor="white" border="2px" width=30% >
<center>

<p style="color:red"><b>Random Number</b> <br><br> <table border="1px" width=30%><tr><center><td style="color:green"> {{randomNumber}}</td></center> </tr>  </table></p>
</center>
 <div class="message">
  <center><button><div @click="clear" class="btn">CLEAR</div></button></center>
  <br>


<center><button style="color:green" @click="random()">Random Number</button><br></center>
<center>
<br>
<input type="number" name="input" v-model="input" placeholder="Value">
</center>

<center>
    <br>
<button v-on:click="getAdd()">ADD</button>
<button v-on:click="getSub()">SUBTRACT</button>
<h1>{{count}}</h1>
 
</center>

</div>
  
</table>
</center>
</template>
<script>
export default {
    name:'MyNew',
  data: ()=> {
    return {
        randomNumber:'',
        input:1,
        count:0
    }
    
  },
  
  methods: {
    clear(){
      this.randomNumber = '';
      this.count='';
      this.input='';
    },
    random(){
        this.randomNumber = Math.ceil(Math.random()*100);
    },
   
    getAdd(){
        this.count=parseInt(this.randomNumber)+parseInt(this.input)
    },
    getSub(){
        this.count=parseInt(this.randomNumber)-parseInt(this.input)
    }
  }
}

</script>