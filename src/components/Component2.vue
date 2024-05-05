<template>
    <v-container>
      <v-row justify="center">
        <v-col cols="12" md="8">
          <v-card class="elevation-5">
            <v-card-title class="text-center font-weight-bold italic" style="font-size: 30px; color: red;">Feedback</v-card-title>
            <v-card-subtitle class="text-center">We value your feedback and appreciate you taking the time to share your thoughts with us. Your feedback helps us improve our services to better serve you.</v-card-subtitle>
            
            <v-divider></v-divider>
  
            <v-card-text>
              <v-form @submit.prevent="submitForm">
                <div class="text-center mb-4">
                  <v-rating v-model="rating" empty-icon="mdi-coffee-outline" full-icon="mdi-coffee" color="brown" hover></v-rating>
                </div>
                
                <v-textarea v-model="description" label="Your review:" outlined></v-textarea>
  
                <v-alert v-if="sucMessage" color="success" outlined>{{ sucMessage }}</v-alert>
                <v-alert v-if="errMessage" color="error" outlined>{{ errMessage }}</v-alert>
  
                <v-btn type="submit" class="mt-4" color="primary" block>Submit</v-btn>
              </v-form>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </template>

  <script>
    
    import '@mdi/font/css/materialdesignicons.css';
    import 'bootstrap/dist/css/bootstrap.css';
    
  export default {
    name: 'ComponentTwo',
    data() {
      return {
        rating: null,
        description: '',
        errMessage: '',
        sucMessage: ''
      };
    },
    methods: {
      validate() {
        if (!this.rating) {
          this.errMessage = "Please provide a rating.";
          return false;
        }
        return true;
      },
      submitForm() {
        if (this.validate()) {
          // Simulating API call
          setTimeout(() => {
            this.sucMessage = "Thank you for your feedback! We appreciate it.";
            this.resetForm();
          }, 1000);
        }
      },
      resetForm() {
        this.rating = null;
        this.description = '';
        this.errMessage = '';
      }
    }
  };
  </script>
  
  <style scoped>
  .v-divider {
    margin: 16px 0;
  }
  </style>
  