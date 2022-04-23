<template>
  <v-row style="background: #fff;
">
    <v-col    cols="12" sm="5" md="5" class="d-flex flex-column  mt-3">
  
    
  <v-card
    class="mx-auto rounded-xl mt-4 px-3"

style="width:90%;background:rgba(38, 115, 209, 1);color:#fff"
    outlined
 
  >
    <v-list-item three-line>
      <v-list-item-content>
       
        <v-list-item-title style="color:#fff" class="text-h6  ">
          Balance
        </v-list-item-title>
        <v-list-item-subtitle style="color:#fff;font-size:9px;">Today 20th September 2021</v-list-item-subtitle>
      </v-list-item-content>

   <v-btn  @click="overlay = !overlay" color="#fff" style="color:rgba(38, 115, 209, 1);text-transform:none"  depressed >
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

 
  

   
       <v-card
    class="mx-auto mt-6 rounded-lg"

style="width:80%;background:#fff;color:#fff"
    outlined
  >
    <v-list-item three-line>
      <v-list-item-content>
       
        <v-list-item-title style="color:rgba(55, 80, 111, 1);font-size:18px;"  color="white">
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

     <v-col class="d-sm-block d-none" cols="7">
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

    <v-col class="d-flex d-sm-none justify-center mt-5">
      <span style="font-size:18px;color:rgba(15, 45, 82, 1);" >No Transactions</span>
    </v-col>

      <v-overlay :value="overlay">
        <Wallet class="d-sm-block d-none" style="width:433px"/>
        <v-col style="d-flex flex-column justify-end align-end">
         <Wallet class="d-sm-none d-block" style="width:420px"/>
        </v-col>
      </v-overlay>

      
    
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage',
  data(){
    return{
      overlay:false
    }
  },
  methods:{
     closeOverlay(){
             this.overlay=false
          
         }
  }
}
</script>

<style scoped>
.btn {
  text-transform: unset !important;
}
</style>
