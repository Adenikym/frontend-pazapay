<template>
   <v-form>
    <v-container>
      <v-row>
      

      

         <v-col
          cols="12"
          sm="6"
          md="4"
        >
          <v-text-field
            label="Pin"
            placeholder="Placeholder"
            outlined
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          sm="6"
          md="4"
        >
          <v-text-field
            label="Confirm Pin"
            placeholder="Placeholder"
            outlined
          ></v-text-field>
        </v-col>

<v-btn style="text-transform:none" color="rgba(38, 115, 209, 1)" class="mt-5 rounded-lg ml-3">
 <span style="color:#Fff;"> Change Pin</span>  
</v-btn>

    
      </v-row>
    </v-container>
  </v-form>
</template>

<script>
export default {

}
</script>

<style>

</style>