<template>
  <LayoutHome>
    <img src="img/bannert.png" class="bg" style="" alt="">
  
    <section class="home" id="home">
      <div class="title" style="position: absolute;">
    <div class="text-1">Olá, meu nome é</div>
    
    <div class="text-2">Gabriel Felipe</div>
   
    <div class="text-3">eu sou <span class="typed-text">{{ typedText }}</span><span class="cursor">&nbsp;</span></div>

    <a class="btn" href="https://drive.google.com/file/d/19c3n8m9d834xtwcWy2c3jJwAMHCi9TvZ/view?usp=sharing">Visualizar CV</a>
        
  </div>
    </section>
    <div id="sobremim" class="sobre">
      
        <q-card  class="my-card">
      <q-card-section>
        <div class="text-h6" style="margin: 0 auto; width: 15%;">Sobre mim</div>
        
      </q-card-section>

      <q-separator style="background: black" inset />

      <q-card-section>
        <div style="display:flex;">
        <q-avatar size="310px">
          <img src="img/perfil.png"  alt="">
      </q-avatar>
        <p style="color: black;">Meu nome não é Drevan é Draveeeeeeeeeeeeeeeeeeeeeen, Em Noxus, guerreiros conhecidos como Desafiadores lutam um contra o outro em uma arena onde sangue é derramado e a força é testada, mas nenhum foi tão celebrado como Draven. Antes um soldado, ele descobriu que as multidões apreciavam seu instinto pelo drama e sua habilidade suprema com seus machados giratórios. Viciado no espetáculo de sua própria perfeição impetuosa, Draven jurou derrotar qualquer que seja seu oponente para garantir que seu nome será cantado pelo império para todo o sempre.</p>
    </div>
        
      </q-card-section>
    </q-card>
      
    </div>
    <div id="skils" class="skils">
      
      
    <q-card-section>
      <div class="text-h6" style="margin: 0 auto; width: 5%; color: white">Skils</div>
      
    </q-card-section>

    <q-separator style="background: #00ffff; width: 15%; margin: 0 auto;" inset />

    <q-card-section>
      <table>
        <tr>
          <td v-for="index in 3" :key="index">
            <div class="row justify-center q-gutter-sm">
              <q-card class="my-card" style="width:70%;">
                <img src="img/python.jpg">

                <q-card-section>
                  <div class="text-h6">Our Changing Planet</div>
                  <div class="text-subtitle2">by John Doe</div>
                </q-card-section>

                <q-card-section class="q-pt-none">
        
                </q-card-section>
              </q-card>
            </div>
          </td>
        </tr>
        <tr>
          <td v-for="index in 3" :key="index">
            <div class="row justify-center q-gutter-sm">
              <q-card class="my-card" style="width:70%;">
                <img src="img/python.jpg">

                <q-card-section>
                  <div class="text-h6">Our Changing Planet</div>
                  <div class="text-subtitle2">by John Doe</div>
                </q-card-section>

                <q-card-section class="q-pt-none">
        
                </q-card-section>
              </q-card>
            </div>
          </td>
        </tr>
      </table>
      
    </q-card-section>
  
    
  </div>
  <div id="exp" class="exp">
      
      <q-card  class="my-card">
    <q-card-section>
      <div class="text-h6" style="margin: 0 auto; width: 23%;">Experiencias/cursos</div>
      
    </q-card-section>

    <q-separator style="background: black" inset />

    <q-card-section>
      <div >
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
    <q-carousel
      swipeable
      animated
      v-model="slide"
      thumbnails
      
      style="width:70%;"
    >
      <q-carousel-slide :name="1" img-src="https://cdn.quasar.dev/img/mountains.jpg" />
      <q-carousel-slide :name="2" img-src="https://cdn.quasar.dev/img/parallax1.jpg" />
      <q-carousel-slide :name="3" img-src="https://cdn.quasar.dev/img/parallax2.jpg" />
      <q-carousel-slide :name="4" img-src="https://cdn.quasar.dev/img/quasar.jpg" />
    </q-carousel>
       </div>
      </div>
    </q-card-section>
  </q-card>
    
  </div>
  <div class="projetos" id="projetos">
    <div class="text-h6" style="margin: 0 auto; width: 15%; color: white; padding-left: 3%;">Projetos</div>
    <q-separator style="background: #00ffff; width: 15%; margin: 0 auto;"  inset />
    <q-carousel
      v-model="projeto"
      transition-prev="slide-right"
      transition-next="slide-left"
      swipeable
      animated
      control-color="primary"
      navigation
      padding
      arrows
      style="background: none" 
      height="300px"
      class=" shadow-2 "
    >
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
  
</LayoutHome>
</template>

<style scoped>
#sobremim{
  transition: 3s;
}
.cardimg{
   border: 1px solid black;
   border-radius: 166px;
   width: 25%;
   height: 300px;
}
  .text-h6{
    font-family: "UbuntuRegular", sans-serif;
    font-size: 30px;
  }
.btn{
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
.text-1{
  font-size: 193%;
}
.text-2{
  font-size: 508%;
  font-weight: 500;
}
.text-3{
  font-size: 279%;
}
section{
  padding: 100px 0;
}
.home{
    display: flex;
    background-position: center;
    background-attachment: fixed;
    background-size: cover;
    height: 0px;
    color: #fff;
    min-height: 500px;
    font-family: 'UbuntuRegular',sans-serif;
    width: 100%;
    position: absolute;
    top: 10px
}
.title {
  position: absolute;
  width: 100%;
  height: 80%;
  
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding-left: 10%;
}

p{
  padding: 41px 27px !important;
  font-size: 1.25rem;
  font-family: "Ubuntu",sans-serif;
  padding: 0.5rem;
  font-weight: 500;
  text-align: justify;
  
}
 .typed-text {
  font-weight: 600;
  color:  #00ffff;;
}
.bg{
  width: 100%; 
  height: 100%; 
  position: relative;
}


.btn:hover{
    background-color: transparent;
    border: 3px solid #00ffff;
    color: #00ffff;
}
@keyframes blink {
  0%  { background-color: #ccc; }
  49% { background-color: #ccc; }
  50% { background-color: transparent; }
  99% { background-color: transparent; }
  100%  { background-color: #ccc; }
}


@media screen and (max-width: 700px)  {
    .home{
      min-height: 328px;
    }
   .title{    
    position: absolute;
    width: 100%;
    height: 16%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-left: 4%;
  }
  .text-1{
    font-size: 132%;
  }
  .text-2{
    font-size: 248%;
  }
  .text-3{
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
  data () {
    return {
      words: ['Full Stack', 'Designer', 'Suporte'],
      typedText: '',
      currentWordIndex: 0,
      currentCharIndex: 0,
      typingSpeed: 100,
      eraseSpeed: 50,
      isErasing: false,
      slide: ref(1),
      projeto: ref(1),
    }
  },
  mounted () {
    this.type()
  },
  methods: {
    type () {
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
    
  }
}
</script>