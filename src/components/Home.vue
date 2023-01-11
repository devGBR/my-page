<template>
  <LayoutHome>

    <div class="topo" style="background: url('/img/bgp.png') fixed;">
      <section class="home" id="home">
        <div class="title" style="">
          <div class="text-1">Olá, meu nome é</div>

          <div class="text-2">Gabriel Felipe</div>

          <div class="text-3">eu sou <span class="typed-text">{{ typedText }}</span><span class="cursor">&nbsp;</span>
          </div>

          <a class="btn"
            href="https://drive.google.com/file/d/19c3n8m9d834xtwcWy2c3jJwAMHCi9TvZ/view?usp=sharing">Visualizar CV</a>

        </div>
      </section>
      <div id="sobremim" class="sobre">

        <q-card>
          <q-card-section>
            <div class="text-h6"
              style="display:flex; justify-content: center;  margin: 40px auto; margin-bottom: 20px !important;;">Sobre
              mim</div>

          </q-card-section>

          <q-separator
            style="background: black;  width: 15%; height: 5px; margin: 0 auto; margin-bottom: 50px !important;"
            inset />

          <q-card-section>
            <div style="display:flex; margin-bottom: 50px;">
              <q-avatar size="400px" class="perfil">
                <img src="img/perfil.jpg" alt="">
              </q-avatar>
              <q-card-section>
                <div class="text-3"
                  style="margin-top: 2px; margin-left: 28px; font-family: 'UbuntuRegular', sans-serif;">Olá, sou Gabriel
                  eu trabalho com <span class="typed-text">{{ trabalho }}</span><span class="cursor">&nbsp;</span></div>

                <p style="color: black;">Meu nome não é Drevan é Draveeeeeeeeeeeeeeeeeeeeeen, Em Noxus, guerreiros
                  conhecidos como Desafiadores lutam um contra o outro em uma arena onde sangue é derramado e a força é
                  testada, mas nenhum foi tão celebrado como Draven. Antes um soldado, ele descobriu que as multidões
                  apreciavam seu instinto pelo drama e sua habilidade suprema com seus machados giratórios. Viciado no
                  espetáculo de sua própria perfeição impetuosa, Draven jurou derrotar qualquer que seja seu oponente
                  para garantir que seu nome será cantado pelo império para todo o sempre.</p>
              </q-card-section>
            </div>

          </q-card-section>
        </q-card>

      </div>
    </div>
    <div class="centro" style="background: url('img/bg.png') fixed bottom;">
      <div id="skils" class="skils">


        <q-card-section>
          <div class="text-h6"
            style="display:flex; justify-content: center; color: white; margin: 40px auto; margin-bottom: 20px !important;">
            Skils</div>

        </q-card-section>

        <q-separator
          style="background: #00ffff; width: 15%; height: 5px; margin: 0 auto; margin-bottom: 50px !important;" inset />

        <q-card-section>
          <div class="skil">
            <div class="row justify-center q-gutter-sm" style="width: 300px;" v-for="index in 8" :key="index">
              <q-card class="my-card">


                <q-card-section>
                  <svg xmlns="http://www.w3.org/2000/svg" 
                    viewBox="5.591 3.262 474.801 137.803">
                    <path
                      d="M184.614 61.929c0-14.562-4.152-22.038-12.457-22.447-3.305-.156-6.53.37-9.669 1.589-2.505.896-4.191 1.784-5.078 2.681V78.51c5.312 3.334 10.029 4.884 14.143 4.64 8.703-.577 13.061-7.643 13.061-21.221zm10.244.604c0 7.398-1.735 13.539-5.225 18.422-3.889 5.527-9.279 8.373-16.17 8.529-5.195.165-10.547-1.462-16.054-4.874v31.591l-8.909-3.178v-70.12c1.462-1.793 3.344-3.333 5.624-4.64 5.303-3.09 11.745-4.678 19.329-4.756l.126.126c6.931-.087 12.271 2.759 16.024 8.529 3.5 5.293 5.255 12.077 5.255 20.371zM249.305 83.266c0 9.923-.994 16.794-2.982 20.615-1.998 3.82-5.8 6.871-11.414 9.143-4.552 1.793-9.475 2.768-14.757 2.934l-1.473-5.614c5.371-.73 9.153-1.462 11.346-2.193 4.318-1.462 7.281-3.703 8.909-6.706 1.306-2.446 1.949-7.115 1.949-14.025V85.1c-6.092 2.769-12.476 4.143-19.152 4.143-4.387 0-8.256-1.374-11.59-4.143-3.743-3.012-5.614-6.832-5.614-11.462v-37.08l8.909-3.051v37.321c0 3.986 1.286 7.057 3.859 9.211s5.907 3.188 9.991 3.109c4.084-.088 8.46-1.667 13.109-4.757v-43.54h8.909v48.415zM284.082 88.997a35.51 35.51 0 0 1-2.934.126c-5.039 0-8.968-1.198-11.774-3.606-2.798-2.407-4.201-5.73-4.201-9.971v-35.09h-6.102v-5.604h6.102V19.968l8.899-3.168v18.052h10.01v5.604h-10.01v34.846c0 3.344.896 5.712 2.689 7.097 1.54 1.14 3.987 1.793 7.32 1.959v4.639zM338.023 88.266h-8.909V53.878c0-3.499-.818-6.511-2.446-9.025-1.881-2.847-4.493-4.27-7.847-4.27-4.084 0-9.191 2.154-15.322 6.462v41.221h-8.908V6.069l8.908-2.807V40.7c5.692-4.143 11.911-6.219 18.666-6.219 4.718 0 8.538 1.589 11.463 4.757 2.934 3.167 4.396 7.115 4.396 11.833v37.195h-.001zM385.374 60.526c0-5.595-1.062-10.215-3.178-13.87-2.515-4.454-6.423-6.804-11.706-7.047-9.767.565-14.641 7.563-14.641 20.976 0 6.15 1.014 11.287 3.061 15.41 2.612 5.254 6.531 7.847 11.756 7.759 9.805-.079 14.708-7.818 14.708-23.228zm9.757.058c0 7.964-2.037 14.592-6.102 19.884-4.475 5.927-10.653 8.899-18.539 8.899-7.817 0-13.909-2.973-18.305-8.899-3.987-5.292-5.976-11.92-5.976-19.884 0-7.485 2.154-13.782 6.463-18.909 4.552-5.439 10.536-8.168 17.935-8.168 7.397 0 13.421 2.729 18.061 8.168 4.309 5.127 6.463 11.424 6.463 18.909zM446.205 88.266h-8.909V51.929c0-3.986-1.198-7.096-3.596-9.338-2.398-2.232-5.596-3.314-9.582-3.227-4.229.078-8.256 1.462-12.076 4.143v44.759h-8.909v-45.86c5.127-3.732 9.845-6.17 14.153-7.31 4.064-1.062 7.651-1.589 10.741-1.589 2.114 0 4.104.204 5.975.614 3.499.809 6.346 2.31 8.538 4.513 2.447 2.437 3.665 5.36 3.665 8.782v40.85z"
                      fill="#646464" />
                    <linearGradient id="a" gradientUnits="userSpaceOnUse" x1="-2031.312" y1="275.868" x2="-1922.296"
                      y2="182.075" gradientTransform="matrix(.5625 0 0 -.568 1145.56 166.282)">
                      <stop offset="0" stop-color="#5a9fd4" />
                      <stop offset="1" stop-color="#306998" />
                    </linearGradient>
                    <path
                      d="M60.51 6.398c-4.584.021-8.961.412-12.812 1.094-11.346 2.005-13.406 6.2-13.406 13.938v10.219h26.812v3.406H24.229c-7.792 0-14.616 4.684-16.75 13.594-2.462 10.213-2.571 16.586 0 27.25 1.906 7.938 6.458 13.594 14.25 13.594h9.219v-12.25c0-8.85 7.657-16.656 16.75-16.656h26.781c7.455 0 13.406-6.138 13.406-13.625V21.429c0-7.266-6.13-12.725-13.406-13.938-4.607-.766-9.385-1.115-13.969-1.093zm-14.5 8.218c2.77 0 5.031 2.299 5.031 5.125 0 2.816-2.262 5.094-5.031 5.094-2.779 0-5.031-2.277-5.031-5.094 0-2.826 2.252-5.125 5.031-5.125z"
                      fill="url(#a)" />
                    <linearGradient id="b" gradientUnits="userSpaceOnUse" x1="-1880.151" y1="125.305" x2="-1919.08"
                      y2="180.384" gradientTransform="matrix(.5625 0 0 -.568 1145.56 166.282)">
                      <stop offset="0" stop-color="#ffd43b" />
                      <stop offset="1" stop-color="#ffe873" />
                    </linearGradient>
                    <path
                      d="M91.229 35.054V46.96c0 9.231-7.826 17-16.75 17H47.698c-7.336 0-13.406 6.278-13.406 13.625v25.531c0 7.267 6.318 11.541 13.406 13.625 8.487 2.496 16.626 2.947 26.781 0 6.75-1.954 13.406-5.888 13.406-13.625V92.898H61.104v-3.406h40.187c7.793 0 10.696-5.436 13.406-13.594 2.8-8.398 2.681-16.476 0-27.25-1.926-7.757-5.604-13.594-13.406-13.594H91.229zM76.166 99.71c2.779 0 5.031 2.277 5.031 5.094 0 2.826-2.252 5.125-5.031 5.125-2.77 0-5.031-2.299-5.031-5.125 0-2.816 2.262-5.094 5.031-5.094z"
                      fill="url(#b)" />
                    <path
                      d="M463.554 26.909h1.562v-9.796h3.699v-1.168h-8.962v1.168h3.7v9.796m6.648 0h1.334v-8.947l2.896 8.946h1.485l3.019-8.916v8.917h1.456V15.946h-1.926l-3.299 9.393-2.812-9.393h-2.153v10.963"
                      fill="#646464" />
                    <radialGradient id="c" cx="-3393.238" cy="376.791" r="29.037"
                      gradientTransform="matrix(0 -.2399 -1.0547 0 458.797 -680.1)" gradientUnits="userSpaceOnUse">
                      <stop offset="0" stop-color="#b8b8b8" stop-opacity=".498" />
                      <stop offset="1" stop-color="#7f7f7f" stop-opacity="0" />
                    </radialGradient>
                    <path
                      d="M97.339 134.098c0 3.848-16.087 6.967-35.932 6.967-19.844 0-35.931-3.119-35.931-6.967s16.087-6.968 35.931-6.968c19.845 0 35.932 3.12 35.932 6.968z"
                      opacity=".444" fill="url(#c)" />
                  </svg>

                </q-card-section>

                <q-card-section class="q-pt-none">

                </q-card-section>
              </q-card>
            </div>
          </div>

        </q-card-section>


      </div>
      <div id="exp" class="exp">


        <q-card-section>
          <div class="text-h6"
            style="display:flex; justify-content: center; color: white; margin: 40px auto; margin-bottom: 20px !important;">
            Experiencias/cursos</div>

        </q-card-section>

        <q-separator
          style="background: #00ffff;  width: 15%; height: 5px; margin: 0 auto; margin-bottom: 50px !important;"
          inset />

        <q-card-section>
          <div>
            <div class="row justify-center q-gutter-sm">
              <div style="display: flex;">
                <q-card class="q-ma-sm">
                  <img src="https://cdn.quasar.dev/img/mountains.jpg">

                  <q-card-section>
                    <div class="text-h6">Card #</div>
                    <div class="text-subtitle2">by John Doe</div>
                  </q-card-section>
                </q-card>
              </div>
              <q-carousel swipeable animated v-model="slide" thumbnails style="width:70%;">
                <q-carousel-slide :name="1" img-src="https://cdn.quasar.dev/img/mountains.jpg" />
                <q-carousel-slide :name="2" img-src="https://cdn.quasar.dev/img/parallax1.jpg" />
                <q-carousel-slide :name="3" img-src="https://cdn.quasar.dev/img/parallax2.jpg" />
                <q-carousel-slide :name="4" img-src="https://cdn.quasar.dev/img/quasar.jpg" />
              </q-carousel>
            </div>
          </div>
        </q-card-section>


      </div>
      <div class="projetos" id="projetos">
        <div class="text-h6"
          style="display:flex; justify-content: center; color: white; margin: 40px auto; margin-bottom: 20px !important;">
          Projetos</div>
        <q-separator
          style="background: #00ffff; width: 15%; height: 5px; margin: 0 auto; margin-bottom: 50px !important;" inset />
        <q-carousel v-model="projeto" transition-prev="slide-right" transition-next="slide-left" swipeable animated
          control-color="primary" navigation padding arrows style="background: none" height="300px" class=" shadow-2 ">
          <q-carousel-slide :name="1" class="column no-wrap">
            <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
              <q-img class="rounded-borders col-6 full-height" src="https://cdn.quasar.dev/img/mountains.jpg" />
              <q-img class="rounded-borders col-6 full-height" src="https://cdn.quasar.dev/img/parallax1.jpg" />
            </div>
          </q-carousel-slide>
          <q-carousel-slide :name="2" class="column no-wrap">
            <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
              <q-img class="rounded-borders col-6 full-height" src="https://cdn.quasar.dev/img/parallax2.jpg" />
              <q-img class="rounded-borders col-6 full-height" src="https://cdn.quasar.dev/img/quasar.jpg" />
            </div>
          </q-carousel-slide>
          <q-carousel-slide :name="3" class="column no-wrap">
            <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
              <q-img class="rounded-borders col-6 full-height" src="https://cdn.quasar.dev/img/cat.jpg" />
              <q-img class="rounded-borders col-6 full-height" src="https://cdn.quasar.dev/img/linux-avatar.png" />
            </div>
          </q-carousel-slide>
          <q-carousel-slide :name="4" class="column no-wrap">
            <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
              <q-img class="rounded-borders col-6 full-height" src="https://cdn.quasar.dev/img/material.png" />
              <q-img class="rounded-borders col-6 full-height" src="https://cdn.quasar.dev/img/donuts.png" />
            </div>
          </q-carousel-slide>
        </q-carousel>
      </div>
    </div>
  </LayoutHome>
</template>

<style scoped>
.my-card {
  width: calc(100% - 30px);
  background: #222;
  text-align: center;
  border-radius: 6px;
  padding: 20px 25px;
  cursor: pointer;
  transition: all .3s ease;
  margin-bottom: 40px;
}

.skil {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
}

.topo {

  background-size: 100% !important;
}

#sobremim {
  transition: 3s;
}

.centro {

  background-size: 100% !important;
}

.cardimg {
  border: 1px solid black;
  border-radius: 166px;
  width: 25%;
  height: 300px;
}

.text-h6 {
  font-family: "UbuntuRegular", sans-serif;
  font-size: 50px !important;
}

.btn {
  margin-top: 20px;
  width: 200px;
  height: 60px;
  background-color: #00ffff;
  font-family: 'Ubuntu', sans-serif;
  font-size: 193%;
  color: black;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 13px;
  text-decoration: none;
}

.text-1 {
  font-size: 193%;
}

.text-2 {
  font-size: 508%;
  font-weight: 500;
}

.text-3 {
  font-size: 279%;
}

section {
  padding: 100px 0;
}

.home {
  display: flex;
  color: #fff;
  min-height: 800px;
  font-family: 'UbuntuRegular', sans-serif;
  width: 100%;
  position: static;
  top: 10px;

}

.title {

  width: 100%;


  display: flex;
  flex-direction: column;
  justify-content: center;
  padding-left: 10%;
}

p {
  padding: 0px 27px !important;
  font-size: 1.25rem;
  font-family: "Ubuntu", sans-serif;
  padding: 0.5rem;
  font-weight: 500;
  text-align: justify;

}

.typed-text {
  font-weight: 600;
  color: #00ffff;
  ;
}

.bg {
  width: 100%;
  height: 100%;
  position: relative;
}

.perfil {
  box-shadow: 0px 4px 25px #111 !important;
  transition: 2s ease-out;
}

.perfil:hover {
  box-shadow: 0px 4px 50px #00ffff !important;
  transition: 2s ease-out;
  font-size: 410px !important;
}

.btn:hover {
  background-color: transparent;
  border: 3px solid #00ffff;
  color: #00ffff;
}

@keyframes blink {
  0% {
    background-color: #ccc;
  }

  49% {
    background-color: #ccc;
  }

  50% {
    background-color: transparent;
  }

  99% {
    background-color: transparent;
  }

  100% {
    background-color: #ccc;
  }
}


@media screen and (max-width: 700px) {
  .home {
    min-height: 328px;
  }

  .title {
    position: absolute;
    width: 100%;
    height: 16%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-left: 4%;
  }

  .text-1 {
    font-size: 132%;
  }

  .text-2 {
    font-size: 248%;
  }

  .text-3 {
    font-size: 172%;
  }

}
</style>

<script>
import LayoutHome from '@/Layout/LayoutHome.vue';

import FloatingActionsVue from './FloatingActions.vue';

import { ref } from 'vue'

export default {
  components: {
    LayoutHome,
    FloatingActionsVue
  },
  data() {
    return {
      words: ['Full Stack', 'Designer', 'Suporte'],
      linguagens: ['Laravel', 'Vue.js', 'PHP', 'Javascript', 'Node.js', 'Quasar', 'Bootstrap', 'Vuetify', 'Postgree', 'MySQL', 'React.js', 'Python', 'Tailwind'],
      trabalho: '',
      typedText: '',
      currentWordIndex: 0,
      WIndex: 0,
      CIndex: 0,
      currentCharIndex: 0,
      typingSpeed: 180,
      eraseSpeed: 500,
      IErasing: false,
      isErasing: false,
      slide: ref(1),
      projeto: ref(1),
    }
  },
  mounted() {
    this.type()
    this.linguas()
  },
  methods: {
    type() {
      setInterval(() => {
        if (this.isErasing) {
          if (this.currentCharIndex > 0) {
            this.typedText = this.typedText.substring(0, this.currentCharIndex - 1)
            this.currentCharIndex--

          } else {
            this.isErasing = false
            this.currentCharIndex = 0
            this.currentWordIndex = (this.currentWordIndex + 1) % this.words.length

          }
        } else {
          if (this.currentCharIndex < this.words[this.currentWordIndex].length) {
            this.typedText += this.words[this.currentWordIndex][this.currentCharIndex]
            this.currentCharIndex++

          } else {
            this.isErasing = true

          }
        }
      }, this.typingSpeed)
    },
    linguas() {
      setInterval(() => {
        if (this.IErasing) {
          if (this.CIndex > 0) {
            this.trabalho = this.trabalho.substring(0, this.CIndex - 1)
            this.CIndex--

          } else {
            this.IErasing = false
            this.CIndex = 0
            this.WIndex = (this.WIndex + 1) % this.linguagens.length

          }
        } else {
          if (this.CIndex < this.linguagens[this.WIndex].length) {
            this.trabalho += this.linguagens[this.WIndex][this.CIndex]
            this.CIndex++

          } else {
            this.IErasing = true

          }
        }
      }, this.typingSpeed)
    },

  }
}
</script>