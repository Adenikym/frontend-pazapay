<template>
  <v-row>
      

      

         <v-col
          cols="12"
          sm="6"
          md="4"
        >
          <v-text-field
            label="Full Name"
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
            label="Email Address"
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
            label="Phone Number"
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
            label="Username"
            placeholder="Placeholder"
            outlined
          ></v-text-field>
        </v-col>
 <v-col
        class="d-flex"
        cols="12"
        sm="4"
      >
        <v-select
          :items="items"
          label="Sex"
          outlined
        ></v-select>
      </v-col>

        <v-col
        class="d-flex"
        cols="12"
        sm="4"
      >
        <v-select
          :items="items"
          label="Date of Birth"
          outlined
        ></v-select>
      </v-col>
      </v-row>
</template>

<script>
export default {

}
</script>

<style>

</style>