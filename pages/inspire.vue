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
          { text: 'Iron (%)', value: 'iron' },
        ],
        desserts: [
          {
            name: 'Frozen Yogurt',
            calories: 159,
            fat: 6.0,
            carbs: 24,
            protein: 4.0,
            iron: '1%',
          },
          {
            name: 'Ice cream sandwich',
            calories: 237,
            fat: 9.0,
            carbs: 37,
            protein: 4.3,
            iron: '1%',
          },
          {
            name: 'Eclair',
            calories: 262,
            fat: 16.0,
            carbs: 23,
            protein: 6.0,
            iron: '7%',
          },
          {
            name: 'Cupcake',
            calories: 305,
            fat: 3.7,
            carbs: 67,
            protein: 4.3,
            iron: '8%',
          },
          {
            name: 'Gingerbread',
            calories: 356,
            fat: 16.0,
            carbs: 49,
            protein: 3.9,
            iron: '16%',
          },
          {
            name: 'Jelly bean',
            calories: 375,
            fat: 0.0,
            carbs: 94,
            protein: 0.0,
            iron: '0%',
          },
          {
            name: 'Lollipop',
            calories: 392,
            fat: 0.2,
            carbs: 98,
            protein: 0,
            iron: '2%',
          },
          {
            name: 'Honeycomb',
            calories: 408,
            fat: 3.2,
            carbs: 87,
            protein: 6.5,
            iron: '45%',
          },
          {
            name: 'Donut',
            calories: 452,
            fat: 25.0,
            carbs: 51,
            protein: 4.9,
            iron: '22%',
          },
          {
            name: 'KitKat',
            calories: 518,
            fat: 26.0,
            carbs: 65,
            protein: 7,
            iron: '6%',
          },
        ],
      }
    },
   
  }


</script>
