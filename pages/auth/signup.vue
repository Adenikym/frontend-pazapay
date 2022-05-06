<template>


  <v-col  class="d-flex justify-space-between">
<v-col cols="6" class=" describe d-sm-block d-none">

<v-col cols="8">

    <v-card  style="margin-top:23%" height="115px" rounded-lg color="rgba(255, 255, 255, 0.9)" class="px-5 py-4  offset-2 rounded-xl">
        <span class="ml-2" style="color:rgba(15, 45, 82, 1);font-weight:500;font-size:26px">Account Opening</span>
        <br>
        
        <span class="mt-4 ml-2"  style="color:rgba(15, 45, 82, 1);font-weight:400;font-size:16px;">Open an account with paza today</span>
    </v-card>
    </v-col>
</v-col>
<v-col sm="6" md="6" cols="12">
    <v-col class="d-flex    justify-end px-4 py-4 mt-4">
    
  </v-col>

  <v-card class="col-lg-10 offset-1 mt-6">

    <div class="col-12 d-flex justify-center">
       <div class="">
      <img src="../../assets/Logo.svg" alt="">
  </div>
    </div>

 

 
  <v-form
    ref="form"
    v-model="valid"
    lazy-validation
    class="col-md-10 offset-1"
  >

   <v-text-field
      v-model="name"
    
      :rules="nameRules"
      label="Full Name"
      required
      outlined
        height="45px"
      dense
     
    ></v-text-field>

    <v-text-field
      v-model="email"
      :rules="emailRules"
      label="E-mail"
      required
      outlined
        height="45px"
      dense
    ></v-text-field>

     <v-text-field
      v-model="phone"
    
      :rules="nameRules"
        height="45px"
      label="Phone Number"
      required
      dense
      outlined
    
    ></v-text-field>

     <v-text-field
      v-model="username"
    
      :rules="nameRules"
      label="Username"
      required
      dense
       height="45px"
      outlined
     
    ></v-text-field>

    <v-text-field
      v-model="pass"
     :value="myPass"
      :rules="nameRules"
      label="Password"
      required
      dense
      height="45px"
      outlined
      :append-icon="value ? 'mdi-eye' : 'mdi-eye-off'"
       @click:append="() => (value = !value)"
    :type="value ? 'password' : 'text'"
    ></v-text-field>

  


<div class="d-flex justify-end mt-4">
<v-btn height="40px" depressed color="rgba(38, 115, 209, 1)" style="text-transform:lowercase;"  class="d-flex px-4 col-12">
    <span style="color:#fff;">sign up</span>
</v-btn>
</div>
 

  

    <!-- <v-btn
      :disabled="!valid"
      color="success"
      class="mr-4"
      @click="validate"
    >
      Validate
    </v-btn>

    <v-btn
      color="error"
      class="mr-4"
      @click="reset"
    >
      Reset Form
    </v-btn>

    <v-btn
      color="warning"
      @click="resetValidation"
    >
      Reset Validation
    </v-btn> -->
  </v-form>

  </v-card>

</v-col>
  </v-col>

</template>
<script>
export default {
layout:'auth',
data(){
  return{
    value:String,
    phone:'',
    username:'',
    pass:''
  }
}
}
</script>

<style scoped>
.describe{
    background: url('../../assets/user-smiling.png');
    background-size:contain ;
    background-repeat: no-repeat ;
}

.btn{
    background: transparent;
 
}

::v-deep .v-btn {
  padding-left: 12px;
  padding-right: 12px;
}
</style>