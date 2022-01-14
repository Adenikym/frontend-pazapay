<template>
  <v-form
    ref="form"
    v-model="valid"
    lazy-validation
    dark
    style="background:#fff;width:100%"
    class="py-3"
  >
<div class="d-flex justify-space-between px-2 py-4" style="border-bottom:1px solid grey;">
  <span style="color:rgba(55, 80, 111, 1)">Airtime</span>

    <v-icon @click="closeForm" color="grey">
      mdi-close-circle
    </v-icon>

</div>
    
    <v-col cols="12" class="">

        <h5 style="color:rgba(55, 80, 111, 1)">Select Operator</h5>
        <v-row class="mt-2 mb-3">
            <v-col>
                <img src="../assets/mtn.svg" alt="">
            </v-col>
             <v-col>
                <img src="../assets/airtel.svg" alt="">
            </v-col>
             <v-col>
                <img src="../assets/glo.svg" alt="">
            </v-col>
             <v-col>
                <img src="../assets/9mobile.svg" alt="">
            </v-col>
        </v-row>
    <v-text-field
      v-model="Amout"
      :counter="10"
      :rules="nameRules"
      label="Name"
      required
      color="grey"
      outlined
      placeholder="Amount"
      
    ></v-text-field>

     <v-text-field
      v-model="Amout"
      :counter="10"
      :rules="nameRules"
      label="Name"
      required
      color="grey"
      outlined
      placeholder="Amount"
      
    ></v-text-field>

  

    <!-- <v-btn
      :disabled="!valid"
      color="success"
      class="mr-4"
      @click="validate"
    >
      Validate
    </v-btn>

    <v-btn
      color="error"
      class="mr-4"
      @click="reset"
    >
      Reset Form
    </v-btn>

    <v-btn
      color="warning"
      @click="resetValidation"
    >
      Reset Validation
    </v-btn> -->
    

  <v-btn @click="closeForm" height="50px" class="mt-4 mb-4" style="background: rgba(38, 115, 209, 1);text-transform:none;
" block color="rgba(38, 115, 209, 1);">
 Continue
  </v-btn>

    </v-col>
    
  </v-form>
</template>

<script>
  export default {
    data: () => ({
      valid: true,
      name: '',
      nameRules: [
        v => !!v || 'Name is required',
        v => (v && v.length <= 10) || 'Name must be less than 10 characters',
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
      select: null,
      items: [
        'Item 1',
        'Item 2',
        'Item 3',
        'Item 4',
      ],
      checkbox: false,
      overlay:false
    }),

    methods: {
      validate () {
        this.$refs.form.validate()
      },
      reset () {
        this.$refs.form.reset()
      },
      resetValidation () {
        this.$refs.form.resetValidation()
      },
      closeForm(){
          this.$parent.closeOverlay()
      }
    },
  }
</script>

<style scoped>
.v-text-field--outlined >>> fieldset {
  border-color: rgba(166, 166, 166, 1);
}

  .text-green input {
      color: green !important;
    }



</style>