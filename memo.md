# PortFolio

https://github.com/nuxt/create-nuxt-app


## 追加するもの一覧
yarn add --dev @fortawesome/fontawesome-free
yarn add @nuxtjs/google-analytics
yarn add @nuxtjs/vuetify


# firebase twitter api
https://github.com/kazuyaseki/firebase-for-twitter-api



# vuetify color

// main.styl
$body-font-family = 'PixelMplus', 'ヒラギノ丸ゴ Pro', 'Hiragino Maru Gothic Pro', 'ヒラギノ角ゴ Pro W3', 'Hiragino Kaku Gothic Pro', 'HG丸ｺﾞｼｯｸM-PRO', 'HGMaruGothicMPRO' !important;



$material-light.background = #fff !important;

@import '~vuetify/src/stylus/main.styl'


# 

.animationBtn {
  animation: animScale 4s infinite ease-out;
  transform-origin: 50% 50%;
  animation-play-state:running;
}
@keyframes animScale {
  0% { transform: scale(0.8, 0.8); }
  10% { transform: scale(1.1, 1.1); }
  20% { transform: scale(1, 1); }
  30% { transform: scale(1.1, 1.1); }
  40% { transform: scale(1, 1); }
}

# class break point 

:class="{'ma-0': $vuetify.breakpoint.smAndDown, 'ma-5': $vuetify.breakpoint.mdAndUp}"
    

    
#icon svg
https://www.flaticon.com/


# gitub pages 

(1)yarn genrerate で dist 作る
(2)dist 配下で
(3)git init add commit 
(4)git remote push

