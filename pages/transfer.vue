<template>
  <v-row class="d-flex flex-column justify-center align-center">
    <v-col cols="11" class="">
    
 <div class="mt-4 col-12 px-0">
   <v-card elevation="1" color="#fff" style="width:100%"  class=" d-flex justify-end  align-self-center py-3">
     <v-btn>Top up balance</v-btn>
    
   </v-card>
    <v-row class="mt-1" style="background:rgba(244, 248, 253, 1)">
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
 </div>
    
    </v-col>

    <v-col cols="11" class="" >
      <div style="background:rgba(244, 248, 253, 1)" class="d-flex justify-space-between py-2 px-4">
        <h6>Transfer</h6>

        <v-btn  @click="overlay = !overlay" color="#fff">
          <v-icon>
            mdi-plus
          </v-icon>
          transfer
        </v-btn>
      </div>
      <div class="py-3">
        <h5 class="ml-5">No Transfers</h5>
      </div>

     
  <v-data-table
    :headers="headers"
    :items="desserts"
    :items-per-page="5"
    class="elevation-1"
  ></v-data-table>

    </v-col>
    <v-overlay  :value="overlay">
      <Wallet style="width:450px;" />
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
      }
    },
   
  }


</script>
