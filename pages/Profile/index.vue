<template>
  <v-row class="d-flex flex-column justify-center align-center py-6 px-3">

      <!-- user avatar -->
      <v-avatar style="height:100px;width:100px;">
      <img
        src="../../assets/avatar.png"
        alt="profile picture"
      >
    </v-avatar>
    <!-- <v-file-input
  chips
  hide-input
  small-chips
  truncate-length="15"
>nnnn</v-file-input> -->
    <p class="mt-3">Tap to change picture</p>
   <v-btn class="d-sm-none d-block" text to="/auth/login" color="rgba(255, 148, 143, 1)">Logout</v-btn>
<!-- 
    edit profile form -->

      <v-col cols="12" md="11" sm="11" class="" >
      <div style="background:rgba(244, 248, 253, 1)" class="d-flex  py-3 px-4">
    

        <v-btn style="text-transform:none"  @click="openPersonal" color="#fff">
         
       Personal
        </v-btn>

         <v-btn style="text-transform:none" class="ml-6"  @click="openSecurity" color="#fff">
     Security
        </v-btn>

         <v-btn style="text-transform:none" class="ml-6 d-sm-block d-none"  @click="openPin" color="#fff" >
         
         Transaction Pin
        </v-btn>
      </div>
      <div class="py-3">
      
      </div>

     

  <v-form>
    <v-container>
       <component
          :is="form"
        />
    </v-container>
  </v-form>


    </v-col>

<v-col cols="11"  class="d-flex justify-end px-3">
  <v-btn class="mr-4" color="#fff">
    <span style="text-transform:none">Save</span>
  </v-btn>
</v-col>
  </v-row>
</template>

<script>
export default {
 data: () => ({
      items: ['Foo', 'Bar', 'Fizz', 'Buzz'],
      form:"Personal"
    }),

    methods:{
      openPersonal(){
        this.form="Personal"
      },
      openPin(){
        this.form="Pin"
      },
      openSecurity(){
        this.form="security"
      }
    }
}
</script>

<style scoped>

</style>