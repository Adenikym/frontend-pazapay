<template>


  <v-row class="">
<v-col cols="6" class=" describe">

<v-col cols="8">

    <v-card  style="margin-top:73%" height="115px" rounded-lg color="rgba(255, 255, 255, 0.9)" class="px-5 py-4  offset-2 rounded-xl">
        <span class="ml-2" style="color:rgba(15, 45, 82, 1);font-weight:500;font-size:26px">Account Opening</span>
        <br>
        
        <span class="mt-4 ml-2"  style="color:rgba(15, 45, 82, 1);font-weight:400;font-size:16px;">Open an account with paza today</span>
    </v-card>
    </v-col>
</v-col>
<v-col class="col-6 ">
    <v-col class="d-flex    justify-end px-4 py-4 mt-4">
      <span class="mt-3">Have an account?</span>
      
   <nuxt-link to="/auth/login">    <v-btn  height="50px" text="true" color="rgba(38, 115, 209, 1)" depressed style="background:transparent;border:1.2px solid rgba(38, 115, 209, 1);text-transform:lowercase" class="ml-2 py-4 mr-4 ">Login here</v-btn>
   </nuxt-link>
  </v-col>

  <div class="">
      <img src="../../assets/Logo.svg" alt="">
  </div>

 
  <v-form
    ref="form"
    v-model="valid"
    lazy-validation
    class="col-8"
  >

   <v-text-field
      v-model="name"
    
      :rules="nameRules"
      label="Full Name"
      required
      outlined
     
    ></v-text-field>

    <v-text-field
      v-model="email"
      :rules="emailRules"
      label="E-mail"
      required
      outlined
    ></v-text-field>

     <v-text-field
      v-model="name"
    
      :rules="nameRules"
      label="Phone Number"
      required
      outlined
    
    ></v-text-field>

     <v-text-field
      v-model="name"
    
      :rules="nameRules"
      label="Username"
      required
      outlined
     
    ></v-text-field>

    <v-text-field
      v-model="name"
    
      :rules="nameRules"
      label="Password"
      required
      outlined
      :append-icon="value ? 'mdi-eye' : 'mdi-eye-off'"
    ></v-text-field>

  


<div class="d-flex justify-end mt-4">
<v-btn height="40px" depressed color="rgba(38, 115, 209, 1)" style="text-transform:lowercase;"  class="d-flex px-4 col-5">
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

</v-col>
  </v-row>

</template>
<script>
export default {
layout:'auth'
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