<template>
  <v-app >
    
    <v-content>
      <v-container grid-list-md text-xs-center>
        <nuxt />
      </v-container>
    </v-content>
    <!-- <v-footer
      :fixed="fixed"
      app
    >
      <span>&copy; 2019</span>
    </v-footer> -->
    <v-footer
      class="command_area"
      height="auto"
      :fixed=true>

      <v-container grid-list-md text-xs-center>
        <v-layout row wrap class="">
          <v-flex xs6>
            <v-btn
            :block=true
            :large=true
            color="grey darken-3 white--text">
            <span><i class="far fa-comment-dots"></i> はなす</span>
            </v-btn>
          </v-flex>
          <v-flex xs6>
            <v-btn
            :block=true
            :large=true
            color="grey darken-3 white--text"><i class="fas fa-swords"></i>たたかう</v-btn>
          </v-flex>
          <v-flex xs6>
            <v-btn
            :block=true
            :large=true
            color="grey darken-3 white--text">じゅもん</v-btn>
          </v-flex>
          <v-flex xs6>
            <v-btn
            :block=true
            :large=true
            color="grey darken-3 white--text">さくせん</v-btn>
          </v-flex>
        </v-layout>
      </v-container>



      <!-- <v-spacer></v-spacer>
      <div>&copy; {{ new Date().getFullYear() }}</div> -->
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'bubble_chart',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
<style type="text/css">
@font-face {
	font-family: 'PixelMplus';
	src: url(~assets/font/PixelMplus10-Regular.ttf);
}

.command_area{
  background-color: rgba(0, 0, 0, 0.4)!important;
  border: 2px solid white;
  border-radius: 1em;
}

.v-btn__content {
  font-size: 1.4em;
}
</style>