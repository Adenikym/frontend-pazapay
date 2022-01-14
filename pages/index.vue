<template>
  <v-row style="background: #fff;
">
    <v-col    cols="5" class="d-flex flex-column  mt-3">
  
    
  <v-card
    class="mx-auto rounded-xl mt-4"

style="width:90%;background:rgba(38, 115, 209, 1);color:#fff"
    outlined
 
  >
    <v-list-item three-line>
      <v-list-item-content>
       
        <v-list-item-title style="color:#fff" class="text-h6  ">
          Balance
        </v-list-item-title>
        <v-list-item-subtitle style="color:#fff">Today 20th September 2021</v-list-item-subtitle>
      </v-list-item-content>

   <v-btn color="#fff" style="color:rgba(38, 115, 209, 1);text-transform:none"  depressed >
     Add Money
   </v-btn>

   
    </v-list-item>

    <div  cols="12" class="d-flex flex-row justify-space-between py-3 px-3">
      <v-text
       
        rounded
        text
        text-h5
        color="white"
        style="font-size:30px"
      >
      ₦ 0.00
      </v-text>

      <v-icon color="white">
    mdi-eye 
   </v-icon>
    </div>
  </v-card>

  <div class="px-4 ml-1">
    <h4 style="color:rgba(15, 45, 82, 1) " class="ml-4 mt-6 px-2">Explore</h4>
  </div>

  

   
       <v-card
    class="mx-auto mt-6 rounded-lg"

style="width:80%;background:#fff;color:#fff"
    outlined
  >
    <v-list-item three-line>
      <v-list-item-content>
       
        <v-list-item-title style="color:rgba(55, 80, 111, 1)" class="text-h6" color="white">
       Buy. Shop. Get Reward
        </v-list-item-title>
        <v-list-item-subtitle>Get cashback reward from marketplace
anytime you make a purchase.</v-list-item-subtitle>


      </v-list-item-content>

 

   
    </v-list-item>
   
 <v-btn text color="rgba(38, 115, 209, 1)"   style="text-transform:none">
  Get Started
</v-btn>

  
  </v-card>

   

   
    </v-col>

     <v-col cols="7">
    <v-col style="" cols="11">
    
  <v-card
    class=" px-0 mt-4 "

    outlined
    style="height:80vh"
  >
    <div style="border-bottom:1px solid  rgba(55, 80, 111, 0.35)"  class="py-4 text-overline">
      <h5 style="font-size:18px;font-weight:400;text-transform:none" class="ml-4">No Transactions</h5>
    </div>
    <div style="height:80%;" class="d-flex justify-center align-center">
      <p style="font-size:12px;color:rgba(55, 80, 111, 1)">You do not  have any transactions yet</p>
    </div>

  
  </v-card>

    </v-col>
      
    </v-col>
    
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>

<style scoped>
.btn {
  text-transform: unset !important;
}
</style>
