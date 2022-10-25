<style>
body{
  background-color:tomato;
}
.message{
  padding-bottom: 20px;
  font-weight: bold;
  color: white;
  }
.sub{
  color: white;
}
table, th, td {
  /* border: 1px solid black; */
  border-collapse: collapse;
}
th,td{
  color: white;
  padding-top: 10px;
  padding-bottom: 20px;
  padding-left: 40px;
  padding-right: 20px;
}
td{
  text-align: left;
}
</style>
<template>
  <form @submit.prevent="submit" v-if="!submitted" >
    <div>
      <center>
      <table style="width:40%">
        <tr>
        <th colspan="2" ><h1>Personal Details</h1></th>
        </tr>

      <tr>
      <td><label class="message">First Name </label></td>
      <td><input v-model="fname" name="fname" placeholder="First Name" /></td>
      
      </tr>

      <tr>
      <td><label class="message">Last Name </label></td>
      <td><input v-model="lname" name="lname" placeholder="Last Name" /></td>
      </tr>

      <tr>
      <td><label class="message" >Gender </label></td>
      <td><input type="radio" id="m" value="Male" v-model="picked" />
      <label class="message">Male</label>
      <input type="radio" id="f" value="Female" v-model="picked" />
      <label class="message">Female</label></td>
      </tr>
      
      <tr>
      <td><label class="message">Phone Number </label></td>
      <td><input type="text" name="input" v-model="input" placeholder="Phone Number"></td>
      </tr>

      <tr>
      <td><label class="message">Email-Id </label></td>
      <td><input type="email" v-model="email" name="email" placeholder="Email-id"  required/></td>
      </tr>

      <tr>
      <td><label class="message">State </label></td>
      <td><select v-model="selected" name="state">
      <option disabled value="">Select Option</option>
      <option>Kerala</option>
      <option>Tamil Nadu</option>
      <option>Karnataka</option>
      </select></td>
      </tr>
      <br>
      
      <tr>
      <td>
      </td>
      <td><button v-on:click="submit()">SUBMIT</button></td>
      <!-- <button v-on:click="clear()">Reset</button> -->
      </tr>
      </table>
      </center>



    
    </div>
  </form>
      <div v-if="submitted" class="sub">
        <center>
        <tr>
        <td>
        <h1>Submitted Details</h1>
        <p>First Name : {{fname}}</p>
        <p>Last Name : {{lname}}</p>
        <p>Gender : {{picked}}</p>
        <p>Phone Number : {{input}} </p>
        <p>Email Id : {{email}}</p>
        <p>State : {{selected}}</p>
        </td>
        </tr>
        </center>
      </div>
</template>

<script>

export default {
    name:'MyDemo',
    data(){
      return{
        fname:'',
        lname:'',
        input:'',
        picked:'',
        email:'',
        selected:'',
        submitted:false,       
  
      }
    },
    methods: {
    // clear(){
    //   this.fname,
    //   this.lname,
    //   this.input,
    //   this.state
      
    // },
    // submit(){
    //   this.submitted=true
    // },

    submit(event) {
      event.preventDefault()
      console.log(event)
      // this.submitted=true

      // this.errors = [];
      // if (!this.fname) {
      //   this.errors.push('First name required');
      // }
      // if (!this.lname) {
      //   this.errors.push('Last name required');
      // }
      // if (!this.email) {
      //   this.errors.push('Email required');
      // }
    },

      // validEmail : function(email) {
 
      //       var re = /(.+)@(.+){2,}\.(.+){2,}/;
      //       if(re.test(email.toLowerCase())){
      //           return true;
      //       }
 
      //   },
 
       

    
    // validateEmail(email) {
    //   if (/^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(email)) {
    //     this.errorMessage = '' 
    //   } 
    //   else {
    //     alert("Email invalid!")
    //   }
    // }

  },
  // watch: {
  //   email(value){
  //     this.email = value;
  //     this.validateEmail(value);
  //   }
  // }
}

</script>