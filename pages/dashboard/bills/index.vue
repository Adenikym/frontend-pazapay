<template>
  <v-row  class="px-6 py-2 d-flex justify-center align-center">

<v-col cols="12" md="11"  sm="11" class="d-flex flex-wrap mt-6" style="background: rgba(244, 248, 253, 1);" >

<v-col cols="5" sm="4" md="2"  class="ml-4  d-flex  flex-column justify-center align-center"  >
    <v-card style="height:120px;width:100%" color="#fff" class="d-flex justify-center align-center py-6 px-3">
<img src="../../../assets/wifi.svg" alt="">
</v-card>
<span class="mt-3">Data</span>
</v-col>
<v-col   @click="overlay = !overlay" cols="5" sm="4" md="2" class="ml-4  d-flex flex-column justify-center align-center"  >
    <v-card style="height:120px;width:100%" color="#fff" class="d-flex justify-center align-center py-6 px-3">
<img src="../../../assets/airtime.svg" alt="">
</v-card>
<span class="mt-3">Airtime</span>
</v-col>
<v-col cols="5" sm="4" md="2"  class="ml-4  d-flex flex-column justify-center align-center"  >
    <v-card style="height:120px;width:100%" color="#fff" class="d-flex justify-center align-center py-6 px-3">
<img src="../../../assets/lightbulb.svg" alt="">
</v-card>
<span class="mt-3">Power</span>
</v-col>
<v-col cols="5" sm="4" md="2"  class="ml-4  d-flex flex-column justify-center align-center"  >
    <v-card style="height:120px;width:100%" color="#fff" class="d-flex justify-center align-center py-6 px-3">
<img src="../../../assets/cable.svg" alt="">
</v-card>
<span class="mt-3">Cable</span>
</v-col>

     
</v-col>


     <v-overlay :value="overlay">
        <airtime class="d-sm-block d-none" style="width:433px"/>
        <v-col style="d-flex flex-column justify-end align-end">
         <airtime class="d-sm-none d-block" style="width:420px"/>
        </v-col>
      </v-overlay>
  </v-row>
</template>

<script>

export default {
 
data(){
    return{
         overlay: false,
       
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
span{
    text-align: center;
}
</style>