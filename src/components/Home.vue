<template>
    <div>
        <!-- <h1>Hello from Home Component</h1> -->
        <!-- <h1>{{data}}</h1>
        <h1>{{msg}}</h1> -->
        <!-- <button v-on:click="hello">Call Hello Function</button> -->
    
        <!-- <h1 v-if="show">Conditional Rendering</h1>
        <h1 v-else>Else Block</h1>
        <button v-on:click="display">Toggle</button> -->


        <!-- <h1>{{randomNumber}}</h1>
        <button v-on:click="random">ADD</button> -->

    </div>

</template>

<script>
export default {
    name:'MyHome',
    props: {
        data:String,
        msg:String,
        // randomNumber:Number
    }, 
    // random:{
    //     randomNumber:''
    // },
    data(){
        // return{
        //     show:false
        // }
    },
    methods:{
        // hello(){
        //  alert("Hello function called!!")
        // }
        // display(){
        //     this.show=!this.show
        // },

        // num(){
        //     this.randomNumber=Math.random()

        // }
   
    }
}
</script>