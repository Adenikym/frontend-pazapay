<template>
  <v-row style="background: #fff; 
" class="px-6">
    <v-col    cols="12" sm="12" md="12" class="d-flex flex-column  mt-3 ">

      <v-card style="background:rgba(38, 115, 209, 1);" class="d-flex justify-space-between py-4 px-4 ">

        <div style="color:#fff;" class="col-6">
          <h2 class="page-head">Welcome, Evwidonor Allen</h2>
          <p class="page-sub">Fastest way to pay your bills, recharge your mobile, shop online and do a lot more!</p>
        </div>

        <img src="../../assets/agent-1.png" alt="">

      </v-card>
  
    
  <v-card
    class=" col-4 mt-4 px-3 mb-3" elevation="0" style="width:90%;background: rgba(38, 115, 209, 0.05);
color:#fff"
    outlined
 
  >
    <v-list-item three-line>
      <v-list-item-content>
       
        <v-list-item-title style="color:rgba(55, 80, 111, 1);" class="text-h6  ">
          Balance
        </v-list-item-title>
      
      </v-list-item-content>

   <v-btn  @click="overlay = !overlay" color="#fff" style="color:rgba(55, 80, 111, 1);text-transform:none"  depressed >
     Add Money
   </v-btn>

   
    </v-list-item>

    <div  cols="12" class="d-flex flex-row justify-space-between py-3 px-3">
      <v-text
       
        rounded
        text
        text-h5
        color="rgba(55, 80, 111, 1)"
        style="font-size:30px;color:rgba(55, 80, 111, 1);"
      >
      ₦ 0.00
      </v-text>

      <v-icon color="rgba(55, 80, 111, 1)">
    mdi-eye 
   </v-icon>
    </div>
  </v-card>

 


<div class="mt-6 ml-4 action-head">Quick Actions</div>
<v-col  class="d-flex flex-wrap py-0"  >

<v-col cols="5" sm="4" md="2"  class=" px-0  d-flex  flex-column justify-center align-center"  >
    <v-card style="height:120px;width:100%" color="#fff" class="d-flex justify-center align-center py-6 px-3">
<img src="../../assets/wifi.svg" alt="">
</v-card>
<span class="mt-3">Data</span>
</v-col>
<v-col   @click="overlay = !overlay" cols="5" sm="4" md="2" class="ml-4  d-flex flex-column justify-center align-center"  >
    <v-card style="height:120px;width:100%" color="#fff" class="d-flex justify-center align-center py-6 px-3">
<img src="../../assets/airtime.svg" alt="">
</v-card>
<span class="mt-3">Airtime</span>
</v-col>
<v-col cols="5" sm="4" md="2"  class="ml-4  d-flex flex-column justify-center align-center"  >
    <v-card style="height:120px;width:100%" color="#fff" class="d-flex justify-center align-center py-6 px-3">
<img src="../../assets/lightbulb.svg" alt="">
</v-card>
<span class="mt-3">Power</span>
</v-col>
<v-col cols="5" sm="4" md="2"  class="ml-4  d-flex flex-column justify-center align-center"  >
    <v-card style="height:120px;width:100%" color="#fff" class="d-flex justify-center align-center py-6 px-3">
<img src="../../assets/cable.svg" alt="">
</v-card>
<span class="mt-3">Cable</span>
</v-col>

     
</v-col>
   

   
    </v-col>

     <v-col class="d-sm-block d-none" cols="7">
    <v-col style="" cols="11">
    


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

.action-head{
 /* font-family: Poppins; */
font-size: 18px;
font-weight: 400;
line-height: 27px;
}

.page-head{
  /* font-family: Poppins; */
font-size: 35px;
font-weight: 500;
line-height: 53px;
letter-spacing: 0px;


}

.page-sub{
  /* font-family: Poppins; */
font-size: 18px;
font-weight: 500;
line-height: 27px;
letter-spacing: 0px;


}
</style>
