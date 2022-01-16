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
  <span style="color:rgba(55, 80, 111, 1)">Top up wallet</span>

    <v-icon @click="closeForm" color="grey">
      mdi-close-circle
    </v-icon>

</div>
    
    <v-col cols="12" class="mt-4 ">
    <v-text-field
      v-model="Amout"
     
      :rules="nameRules"
      label="Amount"
      required
      color="grey"
      outlined
      placeholder="Amount"
         class="text-color"
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
    

  <v-btn height="50px" class="mt-4 mb-4" style="background: rgba(38, 115, 209, 1);text-transform:none;
" block color="rgba(38, 115, 209, 1);"
@click="closeForm">
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
      Amount:'',
      nameRules: [
        v => !!v || 'Amount is required',
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

   .text-color >>> .v-text-field__slot input {
    color: grey
  }

  .text-color >>> .v-text-field__slot label {
    color: grey
  }


</style>