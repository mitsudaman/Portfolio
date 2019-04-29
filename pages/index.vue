<template>
  <div>
    <v-layout row wrap justify-center mt-4>
      <v-flex sm8>
        <h2>プロフィール</h2>
      </v-flex>
    </v-layout>
    <v-layout row wrap justify-center mt-5>
      <v-flex sm7  
      class="profile"
      :class="{ profile_active: isProfileActive }"
      @click="clickProfile">
        <v-layout row wrap justify-center>
          <v-flex xs6 sm4>
            <div>
              <img width="100%" src="~/assets/img/mitsudama.png"/>
            </div>
            <div text-center>
              No.???
            </div>
          </v-flex>
          <v-flex xs6 sm4 text-lef
          :class="{'mt-0': $vuetify.breakpoint.smAndDown, 'mt-4': $vuetify.breakpoint.lgAndUp}">
            <div class="pt-4 pl-2 text-xs-left">
              <p>ミツダマ</p>
              <p>えんじにあニセモン</p>
              <p>たかさ 1.7mm</p>
              <p>おもさ りんご3こぶん</p>
            </div>
          </v-flex>
        </v-layout>
        <hr style="border: 1px solid #000;">
        <div class="mt-3">
          <p>ふくおかに せいそくする うぇぶの ぷろぐらまー。</p>
          <p>ぶらっくな かいしゃから すぐいなくなる。2びょう</p>
          <p>かんに 1000もじの コードを かくことができる。</p>
        </div>
      </v-flex>
    </v-layout>




    <v-layout row wrap justify-center mt-5>
      <v-flex sm8>
        <h2>おぼえたスキル</h2>
      </v-flex>
    </v-layout>
    <v-layout row wrap justify-center mt-5>
      <v-flex xs5 sm3 >
        <div 
        :class="{ active: isHtmlActive }"
        @click="clickHtml">
          <svg class="skill_svg" viewBox="0 0 512 512" xmlns="http://www.w3.org/2000/svg"><path d="m512 96v384c0 17.679688-14.320312 32-32 32h-448c-17.679688 0-32-14.320312-32-32v-384zm0 0" fill="#e4edfb"/><path d="m0 0h512v128h-512zm0 0" fill="#77959e"/><path d="m64 48h32v32h-32zm0 0" fill="#fff"/><path d="m128 48h32v32h-32zm0 0" fill="#fff"/><path d="m432 80h-224c-8.832031 0-16-7.167969-16-16s7.167969-16 16-16h224c8.832031 0 16 7.167969 16 16s-7.167969 16-16 16zm0 0" fill="#62808c"/><g fill="#9575cd"><path d="m64 265.375v38.625h-32v-38.625h-32v118.625h32v-48h32v48h32v-118.625zm0 0"/><path d="m224 265.375h-96v32h32v86.625h32v-86.625h32zm0 0"/><path d="m384 384h-32v-80l-32 32-32-32v80h-32v-118.625h38.625l25.375 25.378906 25.375-25.378906h38.625zm0 0"/><path d="m512 384h-96v-118.625h32v86.625h64zm0 0"/></g></svg>
        </div>
      </v-flex>
      <v-flex xs5 sm3 offset-xs1 >
        <div 
        :class="{ active: isCssActive }"
        @click="clickCss"> 
          <svg class="skill_svg" viewBox="0 0 512 512" xmlns="http://www.w3.org/2000/svg"><path d="m512 96v384c0 17.679688-14.320312 32-32 32h-448c-17.679688 0-32-14.320312-32-32v-384zm0 0" fill="#e4edfb"/><path d="m0 0h512v128h-512zm0 0" fill="#77959e"/><path d="m64 48h32v32h-32zm0 0" fill="#fff"/><path d="m128 48h32v32h-32zm0 0" fill="#fff"/><path d="m432 80h-224c-8.832031 0-16-7.167969-16-16s7.167969-16 16-16h224c8.832031 0 16 7.167969 16 16s-7.167969 16-16 16zm0 0" fill="#62808c"/><g fill="#9575cd"><path d="m128 400c-26.464844 0-48-21.535156-48-48v-64c0-26.464844 21.535156-48 48-48s48 21.535156 48 48v16h-32v-16c0-8.816406-7.167969-16-16-16s-16 7.183594-16 16v64c0 8.816406 7.167969 16 16 16s16-7.183594 16-16v-16h32v16c0 26.464844-21.535156 48-48 48zm0 0"/><path d="m256 400c-26.464844 0-48-21.535156-48-48h32c0 8.816406 7.167969 16 16 16s16-7.183594 16-16-7.167969-16-16-16c-26.464844 0-48-21.535156-48-48s21.535156-48 48-48 48 21.535156 48 48h-32c0-8.816406-7.167969-16-16-16s-16 7.183594-16 16 7.167969 16 16 16c26.464844 0 48 21.535156 48 48s-21.535156 48-48 48zm0 0"/><path d="m384 400c-26.464844 0-48-21.535156-48-48h32c0 8.816406 7.167969 16 16 16s16-7.183594 16-16-7.167969-16-16-16c-26.464844 0-48-21.535156-48-48s21.535156-48 48-48 48 21.535156 48 48h-32c0-8.816406-7.167969-16-16-16s-16 7.183594-16 16 7.167969 16 16 16c26.464844 0 48 21.535156 48 48s-21.535156 48-48 48zm0 0"/></g></svg>

        </div>
      </v-flex>
    </v-layout>
    <v-layout row wrap justify-center mt-5>
      <v-flex xs5 sm3 >
        <div 
        :class="{ active: isJsActive }"
        @click="clickJs">
          <svg version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	        viewBox="0 0 56 56" style="enable-background:new 0 0 56 56;" xml:space="preserve">
            <g>
              <path style="fill:#E9E9E0;" d="M36.985,0H7.963C7.155,0,6.5,0.655,6.5,1.926V55c0,0.345,0.655,1,1.463,1h40.074
                c0.808,0,1.463-0.655,1.463-1V12.978c0-0.696-0.093-0.92-0.257-1.085L37.607,0.257C37.442,0.093,37.218,0,36.985,0z"/>
              <polygon style="fill:#D9D7CA;" points="37.5,0.151 37.5,12 49.349,12 	"/>
              <path style="fill:#EEAF4B;" d="M48.037,56H7.963C7.155,56,6.5,55.345,6.5,54.537V39h43v15.537C49.5,55.345,48.845,56,48.037,56z"/>
              <g>
                <path style="fill:#FFFFFF;" d="M26.021,42.719v7.848c0,0.474-0.087,0.873-0.26,1.196c-0.174,0.323-0.406,0.583-0.697,0.779
                  c-0.292,0.196-0.627,0.333-1.005,0.41s-0.769,0.116-1.169,0.116c-0.201,0-0.436-0.021-0.704-0.062s-0.547-0.104-0.834-0.191
                  s-0.563-0.185-0.827-0.294c-0.265-0.109-0.488-0.232-0.67-0.369l0.697-1.107c0.091,0.063,0.221,0.13,0.39,0.198
                  s0.353,0.132,0.554,0.191c0.2,0.06,0.41,0.111,0.629,0.157s0.424,0.068,0.615,0.068c0.482,0,0.868-0.094,1.155-0.28
                  s0.439-0.504,0.458-0.95v-7.711H26.021z"/>
                <path style="fill:#FFFFFF;" d="M34.184,50.238c0,0.364-0.075,0.718-0.226,1.06s-0.362,0.643-0.636,0.902s-0.611,0.467-1.012,0.622
                  c-0.401,0.155-0.857,0.232-1.367,0.232c-0.219,0-0.444-0.012-0.677-0.034s-0.468-0.062-0.704-0.116
                  c-0.237-0.055-0.463-0.13-0.677-0.226s-0.399-0.212-0.554-0.349l0.287-1.176c0.127,0.073,0.289,0.144,0.485,0.212
                  s0.398,0.132,0.608,0.191c0.209,0.06,0.419,0.107,0.629,0.144c0.209,0.036,0.405,0.055,0.588,0.055c0.556,0,0.982-0.13,1.278-0.39
                  s0.444-0.645,0.444-1.155c0-0.31-0.105-0.574-0.314-0.793c-0.21-0.219-0.472-0.417-0.786-0.595s-0.654-0.355-1.019-0.533
                  c-0.365-0.178-0.707-0.388-1.025-0.629c-0.319-0.241-0.584-0.526-0.793-0.854c-0.21-0.328-0.314-0.738-0.314-1.23
                  c0-0.446,0.082-0.843,0.246-1.189s0.385-0.641,0.663-0.882s0.602-0.426,0.971-0.554s0.759-0.191,1.169-0.191
                  c0.419,0,0.843,0.039,1.271,0.116c0.428,0.077,0.774,0.203,1.039,0.376c-0.055,0.118-0.119,0.248-0.191,0.39
                  c-0.073,0.142-0.142,0.273-0.205,0.396c-0.064,0.123-0.119,0.226-0.164,0.308c-0.046,0.082-0.073,0.128-0.082,0.137
                  c-0.055-0.027-0.116-0.063-0.185-0.109s-0.167-0.091-0.294-0.137c-0.128-0.046-0.297-0.077-0.506-0.096
                  c-0.21-0.019-0.479-0.014-0.807,0.014c-0.183,0.019-0.355,0.07-0.52,0.157s-0.311,0.193-0.438,0.321
                  c-0.128,0.128-0.229,0.271-0.301,0.431c-0.073,0.159-0.109,0.313-0.109,0.458c0,0.364,0.104,0.658,0.314,0.882
                  c0.209,0.224,0.469,0.419,0.779,0.588c0.31,0.169,0.646,0.333,1.012,0.492c0.364,0.159,0.704,0.354,1.019,0.581
                  s0.576,0.513,0.786,0.854C34.078,49.261,34.184,49.7,34.184,50.238z"/>
              </g>
              <g>
                <path style="fill:#EEAF4B;" d="M19.5,19v-4c0-0.551,0.448-1,1-1c0.553,0,1-0.448,1-1s-0.447-1-1-1c-1.654,0-3,1.346-3,3v4
                  c0,1.103-0.897,2-2,2c-0.553,0-1,0.448-1,1s0.447,1,1,1c1.103,0,2,0.897,2,2v4c0,1.654,1.346,3,3,3c0.553,0,1-0.448,1-1
                  s-0.447-1-1-1c-0.552,0-1-0.449-1-1v-4c0-1.2-0.542-2.266-1.382-3C18.958,21.266,19.5,20.2,19.5,19z"/>
                <circle style="fill:#EEAF4B;" cx="27.5" cy="18.5" r="1.5"/>
                <path style="fill:#EEAF4B;" d="M39.5,21c-1.103,0-2-0.897-2-2v-4c0-1.654-1.346-3-3-3c-0.553,0-1,0.448-1,1s0.447,1,1,1
                  c0.552,0,1,0.449,1,1v4c0,1.2,0.542,2.266,1.382,3c-0.84,0.734-1.382,1.8-1.382,3v4c0,0.551-0.448,1-1,1c-0.553,0-1,0.448-1,1
                  s0.447,1,1,1c1.654,0,3-1.346,3-3v-4c0-1.103,0.897-2,2-2c0.553,0,1-0.448,1-1S40.053,21,39.5,21z"/>
                <path style="fill:#EEAF4B;" d="M27.5,24c-0.553,0-1,0.448-1,1v3c0,0.552,0.447,1,1,1s1-0.448,1-1v-3
                  C28.5,24.448,28.053,24,27.5,24z"/>
              </g>
            </g>
          </svg>

        </div>
      </v-flex>
      <v-flex xs5 sm3 offset-xs1 >
        <div 
        class="balloon1"
        @click="clickCss"> 
          <svg class="skill_svg" viewBox="0 0 512 512" xmlns="http://www.w3.org/2000/svg"><path d="m512 96v384c0 17.679688-14.320312 32-32 32h-448c-17.679688 0-32-14.320312-32-32v-384zm0 0" fill="#e4edfb"/><path d="m0 0h512v128h-512zm0 0" fill="#77959e"/><path d="m64 48h32v32h-32zm0 0" fill="#fff"/><path d="m128 48h32v32h-32zm0 0" fill="#fff"/><path d="m432 80h-224c-8.832031 0-16-7.167969-16-16s7.167969-16 16-16h224c8.832031 0 16 7.167969 16 16s-7.167969 16-16 16zm0 0" fill="#62808c"/><g fill="#9575cd"><path d="m128 400c-26.464844 0-48-21.535156-48-48v-64c0-26.464844 21.535156-48 48-48s48 21.535156 48 48v16h-32v-16c0-8.816406-7.167969-16-16-16s-16 7.183594-16 16v64c0 8.816406 7.167969 16 16 16s16-7.183594 16-16v-16h32v16c0 26.464844-21.535156 48-48 48zm0 0"/><path d="m256 400c-26.464844 0-48-21.535156-48-48h32c0 8.816406 7.167969 16 16 16s16-7.183594 16-16-7.167969-16-16-16c-26.464844 0-48-21.535156-48-48s21.535156-48 48-48 48 21.535156 48 48h-32c0-8.816406-7.167969-16-16-16s-16 7.183594-16 16 7.167969 16 16 16c26.464844 0 48 21.535156 48 48s-21.535156 48-48 48zm0 0"/><path d="m384 400c-26.464844 0-48-21.535156-48-48h32c0 8.816406 7.167969 16 16 16s16-7.183594 16-16-7.167969-16-16-16c-26.464844 0-48-21.535156-48-48s21.535156-48 48-48 48 21.535156 48 48h-32c0-8.816406-7.167969-16-16-16s-16 7.183594-16 16 7.167969 16 16 16c26.464844 0 48 21.535156 48 48s-21.535156 48-48 48zm0 0"/></g></svg>

        </div>
      </v-flex>
      <div id="stick">
        <div id="sky"></div>
        <div id="ground"></div>
        <div id="head"></div>
        <div id="upper_arm_left"></div>
        <div id="body"></div>
        <div id="upper_thigh_left"></div>
        <div id="upper_thigh_right"></div>
      </div>
    </v-layout>


    <v-layout row wrap justify-center mt-5>
      <v-flex sm8>
        <h2>召喚サービス</h2>
      </v-flex>
    </v-layout>
    <v-layout row wrap justify-center mt-3>
      <v-flex xs12 sm5 mt-4 >
        <div
        :class="{ active: isBbsWikiActive }"
        @click="clickBbsWiki">
          <img class="card" width="100%" src="~/assets/img/bbswiki.png"/>
        </div>
        <div class="service_title">BBSWiki</div>
      </v-flex>
    </v-layout>
    <v-layout row wrap justify-center mt-5>
      <v-flex xs12 sm5>
        <div
        :class="{ active: isTSMakerActive }"
        @click="clickTSMaker">
          <img class="card" width="100%" src="~/assets/img/TSMaker.png"/>
        </div>
        <div class="service_title">時間割メーカー</div>
      </v-flex>
    </v-layout>
    <v-layout row wrap justify-center mt-5>
      <v-flex xs12 sm5 >
        <div
        :class="{ active: isHaikuMakerActive }"
        @click="clickHaikuMaker">
          <img class="card" width="100%" src="~/assets/img/HaikuMaker_ogp.jpg"/>
        </div>
        <div class="service_title">俳句メーカー</div>
      </v-flex>
    </v-layout>
    <v-layout row wrap justify-center mt-5>
      <v-flex xs12 sm5>
        <div
        :class="{ active: isChoiceMakerActive }"
        @click="clickChoiceMaker">
          <img class="card" width="100%" src="~/assets/img/ogp.jpg"/>
        </div>
        <div class="service_title">究極の選択メーカー</div>
      </v-flex>
    </v-layout>
  </div>
</template>
<script>
import { mapMutations } from 'vuex'
export default {
  data () {
    return {
      isProfileActive: false,
      isHtmlActive: false,
      isCssActive: false,
      isJsActive: false,
      isBbsWikiActive: false,
      isTSMakerActive: false,
      isHaikuMakerActive: false,
      isChoiceMakerActive: false,
    }
  },
  methods: {
    next() {
      this.flg = !this.flg
      console.log(this.flg) 
    },
    clickProfile(){
      this.resetActive()
      this.isProfileActive = true;
      this.$store.commit('comment/change', this.$store.state.comment.commentList.myself)
    },
    clickHtml(){
      this.resetActive()
      this.isHtmlActive = true;
      this.$store.commit('comment/change', this.$store.state.comment.commentList.html)
    },
    clickCss(){
      this.resetActive()
      this.isCssActive = true;
      this.$store.commit('comment/change', this.$store.state.comment.commentList.css)
    },
    clickJs(){
      this.resetActive()
      this.isJsActive = true;
      this.$store.commit('comment/change', this.$store.state.comment.commentList.javascript)
    },
    clickBbsWiki(){
      this.resetActive()
      this.isBbsWikiActive = true;
      this.$store.commit('comment/change', this.$store.state.comment.commentList.bbswiki)
    },
    clickTSMaker(){
      this.resetActive()
      this.isTSMakerActive = true;
      this.$store.commit('comment/change', this.$store.state.comment.commentList.TSMaker)
    },
    clickHaikuMaker(){
      this.resetActive()
      this.isHaikuMakerActive = true;
      this.$store.commit('comment/change', this.$store.state.comment.commentList.HaikuMaker)
    },
    clickChoiceMaker(){
      this.resetActive()
      this.isChoiceMakerActive = true;
      this.$store.commit('comment/change', this.$store.state.comment.commentList.ChoiceMaker)
    },
    resetActive(){
      this.isProfileActive = false;
      this.isHtmlActive = false;
      this.isCssActive = false;
      this.isJsActive = false;
      this.isBbsWikiActive = false;
      this.isTSMakerActive = false;
      this.isHaikuMakerActive = false;
      this.isChoiceMakerActive = false;
    }
  }
}
</script>

<style type="text/css">
h2 {
  font-size: 2.5em;
  border: 2px solid black;
  border-radius: 1em;
}
.skill_svg {
  font-size: 1.6em;
  border-radius: 1em;
}
.card {
  font-size: 1.6em;
  border: 2px solid black;
  border-radius: 1em;
}
.active {
  position: relative;
  display: inline-block;
  min-width: 100%;
}

.active:before {
  content: "";
  position: absolute;
  top: -25px;
  left: 50%;
  margin-left: -15px;
  border: 15px solid transparent;
  border-top: 15px solid #000;
  animation: Flash1 1s infinite;
}

.profile {
  border: 6px double #000;
}
.profile_active {
  border-color: #0000ff;
}
.service_title{
  font-size: 2em;
}




</style>