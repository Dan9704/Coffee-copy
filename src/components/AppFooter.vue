<template>
    <v-container class="align-middle text-center" fluid>
      <v-card class="elevation-2 footer-background">
        <v-card-title>Contact Us:</v-card-title>
        <v-card-actions class="justify-center">
          <v-btn icon :href="'https://www.instagram.com/maples_cafe_footscray/'" target="_blank" v-tooltip.bottom="{ content: 'Follow us on Instagram' }">
            <v-icon>mdi-instagram</v-icon>
          </v-btn>
          <v-btn icon :href="'https://www.facebook.com/maplescafefootscray'" target="_blank" v-tooltip.bottom="{ content: 'Like us on Facebook' }">
            <v-icon>mdi-facebook</v-icon>
          </v-btn>
          <v-btn icon :href="'mailto:duongcrseven@gmail.com'" v-tooltip.bottom="{ content: 'Send us an email' }">
            <v-icon>mdi-email</v-icon>
          </v-btn>
          <v-btn icon :href="'https://api.whatsapp.com/send?phone=yourphonenumber'" target="_blank" v-tooltip.bottom="{ content: 'Message us on WhatsApp' }">
            <v-icon>mdi-whatsapp</v-icon>
          </v-btn>
          <v-btn icon :href="'tel:0488315327'" v-tooltip.bottom="{ content: 'Call us' }">
            <v-icon>mdi-phone</v-icon>
          </v-btn>
        </v-card-actions>
        <v-card-text>
          © 2024 Maples Cafe. All Rights Reserved.
        </v-card-text>
      </v-card>
    </v-container>
  </template>
  
  <script>
  export default {
    name: 'AppFooter',
  };
  </script>
  
  <style>
  .footer-background {
    background-color: #333; /* Dark background for footer */
    color: #fff; /* White text color */
    padding: 20px 0; /* Top and Bottom padding */
  }
  </style>
  













<!-- <template>
    <v-container class="align-middle text-center">
        <v-card class="elevation-2">
            <v-card-title>Contact Us:</v-card-title>
            <v-card-actions class="justify-center">
                <v-btn icon>
                    <v-icon>mdi-instagram</v-icon>
                </v-btn>
                <v-btn icon>
                    <v-icon>mdi-facebook</v-icon>
                </v-btn>
                <v-btn icon>
                    <v-icon>mdi-email</v-icon>
                </v-btn>
                <v-btn icon>
                    <v-icon>mdi-whatsapp</v-icon>
                </v-btn>
                <v-btn icon>
                    <v-icon>mdi-phone</v-icon>
                </v-btn>
            </v-card-actions>
        </v-card>
    </v-container>
</template>
<script>
export default {
    name: 'AppFooter',
};
</script> -->