<template>
  <v-row class="d-flex flex-column justify-center align-center">
    <v-col cols="11" class="">
    
 <div class="mt-4 col-12 px-0">
   <div elevation="1" color="#fff" style="width:100%"  class=" d-flex justify-end  align-self-center py-3">
     <v-btn class="d-sm-block d-none"  @click="overlay = !overlay" color="#fff" style="text-transform:none; font-size:15px">Top up balance</v-btn>
    
   </div>
    <v-row class="mt-1 d-sm-flex d-none" style="background:rgba(244, 248, 253, 1)">
       <v-col style="border-right:1px solid rgba(55, 80, 111, 0.35);" cols="4" class=" d-flex flex-column justify-center align-center py-4">
  <v-text
       
        rounded
        text
        text-h5
        color="white"
        style="font-size:30px;color:rgba(38, 115, 209, 1)"
      >
      ₦ 0.00
      </v-text>
      <p class="mt-1">AVAILABLE BALANCE</p>
       </v-col>
       <v-col style="border-right:1px solid rgba(55, 80, 111, 0.35);" cols="4" class=" d-flex flex-column justify-center align-center py-4">
  <v-text
       
        rounded
        text
        text-h5
        color="white"
        style="font-size:30px;color:rgba(38, 115, 209, 1)"
      >
      ₦ 0.00
      </v-text>
      <p class="mt-1">TOTAL AMOUNT TRANSFERRED</p>
       </v-col>
       <v-col style="border-right:1px solid rgba(55, 80, 111, 0.35);" cols="4" class=" d-flex flex-column justify-center align-center py-4">
  <v-text
       
        rounded
        text
        text-h5
        color="white"
        style="font-size:30px;color:rgba(38, 115, 209, 1)"
      >
      0
      </v-text>
      <p class="mt-1">SUCCESSFUL TRANSFERS </p>
       </v-col>
  
     </v-row>


     <!-- mobile carousel -->


  <v-carousel style="height:150px" v-model="model" class="d-sm-none d-block rounded-lg"  hide-delimiter-background
    show-arrows-on-hover cycle>
    <v-carousel-item
      v-for="(color, i) in colors"
      :key="i"
   
    >
      <v-sheet
        color="rgba(38, 115, 209, 1)"
        height="100%"
      class="px-5 py-2"
      >
        <v-row
          class="fill-height"
      
        
        >
          <div class="py-4 px-4 mt-5">
        <p style="font-size:18px;color:#fff;line-height:15px;">  {{color.title }}</p>  
        <span style="font-size:28px;color:#fff;">{{color.amount}}</span>
          </div>
        </v-row>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>

 </div>
    
    </v-col>

    <v-col cols="11" class="" >

      <div  style="background:rgba(244, 248, 253, 1)" class="d-sm-flex d-none justify-space-between py-4 px-4">
        <h6 style="font-size:18px;color:rgba(55, 80, 111, 1);font-weight:400;">Transfer</h6>

        <v-btn color="rgba(38, 115, 209, 1)"  @click="overlay = !overlay" >
          <v-icon style="color:#fff">
            mdi-plus
          </v-icon>
      <span style="color:#fff;text-transform:none;font-size:15px">New  Transfer</span>  
        </v-btn>
      </div>

      <div  class="d-sm-none d-flex justify-space-between py-4 px-4 col-12">
       <v-btn  @click="overlay = !overlay" color="#fff" style="text-transform:none; font-size:15px">Top up balance</v-btn>
    

        <v-btn color="rgba(38, 115, 209, 1)"  @click="overlay = !overlay" >
          <v-icon style="color:#fff">
            mdi-plus
          </v-icon>
      <span style="color:#fff;text-transform:none;font-size:15px">New  Transfer</span>  
        </v-btn>
      </div>


      <div class="py-3">
        <h5 style="color:rgba(55, 80, 111, 1);font-size:14px;font-weight:400" class="ml-5">No Transfers</h5>
      </div>

     
  <v-data-table
    :headers="headers"
    :items="desserts"
    :items-per-page="5"
    class="elevation-1"
  ></v-data-table>

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


    data () {
      return {
          overlay: false,
        headers: [
          {
            text: 'Receiver',
            align: 'start',
            sortable: false,
            value: 'name',
          },
          { text: 'Amount', value: 'calories' },
          { text: 'Transfer Type', value: 'fat' },
          { text: 'Status', value: 'carbs' },
          { text: 'Date', value: 'protein' },
        
        ],
        desserts: [
       
        ],
         model: 0,
      colors: [
      {title:"Available Balance", amount:"₦ 0.00"},
      {title:"Total Amount Transferred", amount:"₦ 0.00"},
      {title:"Successful Transfers", amount:0},
      
      ],
      }
    },
   methods:{
      closeOverlay(){
             this.overlay=false
          
         }
   }
  }


</script>
