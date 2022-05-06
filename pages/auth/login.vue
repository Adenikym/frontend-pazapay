<template>


  <v-row class="">
<v-col  cols="6" class=" describe d-sm-block d-none">

 <v-col cols="8">

    <v-card style="margin-top:28%" height="115px"  rounded-lg color="rgba(255, 255, 255, 0.9)" class="px-5 py-4 offset-2 rounded-xl">
        <span class="ml-2" style="color:rgba(15, 45, 82, 1);font-weight:500;font-size:26px">Login</span>
        <br>
        
        <span class="mt-4 ml-2"  style="color:rgba(15, 45, 82, 1);font-weight:400;font-size:16px;">Login to your account to get started</span>
    </v-card>

    </v-col>
</v-col>
<v-col  sm="6" md="6" cols="12" class="d-flex flex-column align-center justify-center ">


  <v-card  class="mt-6 col-10">

  <div class="">
      <img src="../../assets/Logo.svg" alt="">
  </div>

 
  <v-form
    ref="form"
    v-model="valid"
    lazy-validation
 class="col-md-12 "
  >

    <v-text-field
      v-model="email"
      :rules="emailRules"
      label="E-mail"
      required
      outlined
      type="email"
    ></v-text-field>

    <v-text-field
      v-model="name"
     :value="myPass"
      :rules="nameRules"
      label="Password"
      required
      outlined
      :append-icon="value ? 'mdi-eye' : 'mdi-eye-off'"
       @click:append="() => (value = !value)"
    :type="value ? 'password' : 'text'"
    ></v-text-field>

  
<v-btn style="text-transform:none" text="true" color="rgba(38, 115, 209, 1)" nuxt>
    Forgot Password
</v-btn>

<div class="d-flex  mt-4">

<v-btn height="40px" depressed color="rgba(38, 115, 209, 1)" style="text-transform:lowercase;"  class="col-12  px-4">
    <span style="color:#fff;">Login to your account</span>
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

     <v-col class="d-flex    px-4  ">
      <span class="mt-2">Don't have an account?</span>
      
 <v-btn text   color="rgba(38, 115, 209, 1)" depressed style="background:transparent;text-transform:none" class="ml-2 mr-4">Sign up here</v-btn>
  
  </v-col>

  </v-card>

</v-col>
  </v-row>

</template>
<script>
export default {
layout:'auth',
data(){
  return{
    value:String,
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