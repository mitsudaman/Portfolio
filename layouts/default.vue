<template>
  <v-app >
    <v-content>
      <v-container grid-list-md text-xs-center class="mb-6">
        <nuxt class=""/>
      <v-layout 
      row wrap justify-center
      class="footer-fixed">
        <v-flex
          d-flex
          xs11
          sm5
          class="balloon_area pa-3"
        > 
          <div
            v-if="!commentFlg">
            <v-layout row wrap>
              <v-flex xs6>
                <v-btn
                :block=true
                :large=true
                @click="commandTalk"
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
          </div>


          <div
            v-if="commentFlg"
            @click="commentNext">
            <v-layout row wrap>
              <v-flex xs12 class="comment text-xs-left">
                <p>{{$store.state.comment.content[commentContentIndex]}}</p>
                <p class="next-arrow text-xs-center">▼</p>
              </v-flex>
            </v-layout>
          </div>

        </v-flex>
      </v-layout>
      </v-container>
    </v-content>

      

    <!-- <v-footer
      height="auto"
      :fixed=true>
あああああああああああ
    </v-footer> -->

    
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      commentFlg: false,
      commentContentIndex: 0,
    }
  },
  methods: {
    commandTalk(){
      this.commentFlg = true;
      this.commentContentIndex = 0
    },
    commentNext() {
      if(this.$store.state.comment.content.length == this.commentContentIndex+1){
        this.commentFlg = !this.commentFlg
      }else{
        this.commentContentIndex ++
      }
    }
  }
}
</script>
<style type="text/css">
@font-face {
	font-family: 'PixelMplus';
	src: url(~assets/font/PixelMplus10-Regular.ttf);
}

.balloon_area{
  background-color: rgba(0, 0, 0, 0.6)!important;
  border: 2px solid white;
  border-radius: 1em;
}

.v-btn__content {
  font-size: 1.4em;
}
.comment{
  color: white;
  font-size: 1.4em;
  margin-bottom: 0px;
}
.comment p {
  margin-bottom: 0px;
}

.next-arrow{
  animation: Flash1 1s infinite;
}
/* アニメーション */
@keyframes Flash1{
  50%{
    opacity: 0;
  }
}

.mb-6 {
  margin-bottom: 200px !important;
}

.footer-fixed {
    position: fixed;
}

.footer-fixed {
  margin-left: 1px;
  bottom: 5px;
  left: 6px;
  width: 99%;
  z-index: 3;
}
.sidemenu:before {
    background-color: #000;
    color: #fff;
    content: "ああああああああ";
    position: relative;
    left: 45px;
    top: 12px;
}
</style>