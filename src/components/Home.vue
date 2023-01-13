<template>
  <LayoutHome>

    <div class="topo" style="background: url('/img/bgp.png')  top no-repeat fixed ;">
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
            <div class="card-sobre" >
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
            <div class="row justify-center q-gutter-sm" style="width: 300px;" v-for="sk, index in sk" :key="index">
              <q-card class="my-card" style="width: calc(100% - 30px) !important;">


                <q-card-section>
                  <img  style="width: 100%; height:100%; border-radius: 7px !important;" :src="sk.image" alt="" >

                </q-card-section>

                <q-card-section class="q-pt-none" :style="sk.color" style="font-size: 30px; font-family: 'UbuntuRegular';">
                    {{ sk.name }}
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
            Experiencias</div>
        </q-card-section>

        <q-separator
          style="background: #00ffff;  width: 15%; height: 5px; margin: 0 auto; margin-bottom: 50px !important;"
          inset />

        <q-card-section>
          <div>
            <div class="row justify-center q-gutter-sm">
              <div style="display: flex;">
                <q-card class="profissao">
                  <img src="img/logocge.png" style="
    height: 470px; width: 400px;
">

                  <q-card-section>
                    <div class="text-h6 text" style="color: #00ffff; margin-left: 3px;  margin-bottom: 30px !important; font-size: 27px !important;">Controladoria Geral do Estado do Amapá </div>
                    <div class="sub" style="margin-top: 10px; margin-left: 35px; font-size: 30px !important; font-family: 'Ubuntu',sans-serif; color: #999; font-style: italic;">Estágiario</div>
                    <div class="text-h5" style="margin-top: 20px; margin-left: 10px; font-size: 20px !important;"> • <span class="conteudo">Coordenadoria de Tecnologia da Informação - CTEC</span></div>
                    <div class="text-h5" style="margin-top: 20px; font-size: 20px !important;">Descrição: 
                      <div class="conteudo" style="margin-left: 20px; font-size: 13px; display: grid;"> 
                          <div>• Desenvolvimento de aplicações web e programas em php, laravel, vue js, python.</div>
                          <div>• Manutenção de sistemas web desenvolvidos em PHP com base de dados PostgreSQL.</div>
                          <div>• Suporte TI. </div>
                      </div>
                  </div>
                  </q-card-section>
                </q-card>
              </div>
              
            </div>
          </div>
        </q-card-section>
        <q-card-section>
          <div class="text-h6"
            style="display:flex; justify-content: center; color: white; margin: 40px auto; margin-bottom: 20px !important;">
            Cursos</div>
        </q-card-section>

        <q-separator
          style="background: #00ffff;  width: 15%; height: 5px; margin: 0 auto; margin-bottom: 50px !important;"
          inset />

          <q-card-section>
            <q-card-section>
          <div class="text-h6"
            style="display:flex; justify-content: center; color: white; margin: 40px auto; margin-bottom: 20px !important;">
            Certificados</div>
        </q-card-section>
            <div style="">
              <div class="row justify-center q-gutter-sm">
                <div style="display: flex; width: 942px; height: 600px; justify-content: center;">
                  
                  <q-carousel swipeable animated v-model="slide" thumbnails style="width: 100%; height: 100%;">
                    <q-carousel-slide :name="1" style="background-size: 100%;" img-src="certificados/arduino.png" />
                    <q-carousel-slide :name="2" style=" width:100%;" img-src="certificados/science.png" />
                    <q-carousel-slide :name="3" style=" width:100%;" img-src="certificados/Enap.png" />
                    <q-carousel-slide :name="4" style=" width:100%;" img-src="certificados/tifgv.png" />
                    <q-carousel-slide :name="5" style=" width:100%;" img-src="certificados/vuejs.png" />
                    <q-carousel-slide :name="6" style=" width:100%;" img-src="certificados/css.png" />
                    <q-carousel-slide :name="7" style=" width:100%;" img-src="certificados/html.png" />
                    <q-carousel-slide :name="8" style=" width:100%;" img-src="certificados/infocus.png" />
                  </q-carousel>
                </div>
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
          control-color="primary" navigation padding arrows style="background: none" height="600px" class=" shadow-2 ">
          <q-carousel-slide :name="1" class="column no-wrap">
            <div class="row fit  items-center q-gutter-xs q-col-gutter no-wrap" style="display: flex; ">

              <q-card class="my-card">
                 <q-card-section>
                     
                  <img src="img/Logocge.png" style="width: 30%; height: 30%;">
                    
                </q-card-section>
                <q-card-section class="q-pt-none">
                    
                </q-card-section>
                <div class="text titlepj" style=""><div class="textitlepj">Sistema de Monitoramento de Contratos - CGEAP</div></div>
              </q-card>
             
              <q-card class="my-card">
                                       
                <q-card-section>

                      <img src="img/Logo.png" style="width: 30%; height: 30%;">   

                </q-card-section>
                <q-card-section class="q-pt-none">
                    
                </q-card-section> 
                <div class="text titlepj" style=""><div class="textitlepj">JOPE</div></div>
              </q-card>
              <q-card class="my-card">
                    
                <q-card-section>
                      
                  <img src="img/mf.png" style="width: 30%; height: 30%!important;">
                    
                </q-card-section>

                <q-card-section class="q-pt-none">
                    
                </q-card-section>
                <div class="text titlepj" style=""><div class="textitlepj">Recriação Mirror Fashion</div></div>
              </q-card>

            </div>
          </q-carousel-slide>
          <q-carousel-slide :name="2" class="column no-wrap">
            <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
              <q-card class="my-card">
                 <q-card-section>
                     
                  <img src="img/Logo-GLPI-250-black.png" style="width: 30%; height: 30%;">
                    
                </q-card-section>
                <q-card-section class="q-pt-none">
                    
                </q-card-section>
                <div class="text titlepj" style="">
                  <div class="textitlepj">Implementação do GLPI na CGEAP</div>
                </div>
              </q-card>
              <q-card class="my-card">
                                       
                <q-card-section>

                      <img src="img/eTransportes.png" style="width: 30%; height: 30%;">   

                </q-card-section>
                <q-card-section class="q-pt-none">
                    
                </q-card-section> 
                <div class="text titlepj" style=""><div class="textitlepj">eTransporte - CGEAP</div></div>
              </q-card>
              <q-card class="my-card">
                    
                <q-card-section>
                      
                  <img src="img/logoGETQ.png" style="width: 30%; height: 30%!important;">
                    
                </q-card-section>

                <q-card-section class="q-pt-none">
                    
                </q-card-section>
                <div class="text titlepj" style=""><div class="textitlepj">Sistema De Gerenciamento de Estoque</div></div>
              </q-card>
            </div>
          </q-carousel-slide>
          <q-carousel-slide :name="3" class="column no-wrap">
            <div class="row fit justify-center items-center q-gutter-xs q-col-gutter no-wrap">
              <q-card class="my-card">
                 <q-card-section>
                     
                  <img src="img/sr.png" style="width: 30%; height: 30%;">
                    
                </q-card-section>
                <q-card-section class="q-pt-none">
                    
                </q-card-section>
                <div class="text titlepj" style=""><div class="textitlepj">Pizzaria Santa Rita</div></div>
              </q-card>
              <q-card class="my-card">
                                       
                <q-card-section>

                      <img src="img/py.png" style="width: 30%; height: 30%;">   

                </q-card-section>
                <q-card-section class="q-pt-none">
                    
                </q-card-section> 
                <div class="text titlepj" style=""><div class="textitlepj">Programa em Python criador de array php</div></div>
              </q-card>
         
              <q-card class="my-card">
                                       
                <q-card-section>

                      <img src="img/mario.gif" style="width: 30%; height: 30%;">   

                </q-card-section>
                <q-card-section class="q-pt-none">
                    
                </q-card-section> 
                <div class="text titlepj" style=""><div class="textitlepj">Jogo do Mario Simples</div></div>
              </q-card>
            </div>
          </q-carousel-slide>
         
        </q-carousel>
      </div>
    </div>
  </LayoutHome>
</template>

<style scoped>
.titlepj{
    width: 500px;
    display: flex !important;
    justify-content: center !important;
    position: absolute;
    margin-top: 25px;
}
.textitlepj{
  color: rgb(255, 255, 255);
  font-size: 20px !important;
}
.card-sobre{
    display:flex !important; 
    margin-bottom: 50px;
}
.my-card {
  width: calc(37% - 30px);
  background: #222;
  text-align: center;
  border-radius: 6px;
  padding: 20px 25px;
  cursor: pointer;
  transition: all .3s ease;
  margin-bottom: 40px;
}
.profissao{
  background: #222;
  display: flex;
  flex-direction: column;
  align-items: center;
}


.skil {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  margin-left: 100px;
  margin-right: 100px;
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
.text{
  display: flex;
 
  justify-content: center;
  font-family: 'UbuntuMedium', sans-serif !important;
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
.text-h5{
  font-size: 34px;
  font-family: 'UbuntuMedium',sans-serif;
  color: #00ffff;
}
.conteudo{
  font-size: 21px;
  font-family: 'UbuntuRegular';
  color: #ccc;
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
@media screen and ( max-width: 855px){
  .card-sobre{
    display: flex;
    margin-bottom: 50px;
    flex-wrap: wrap;
    justify-content: center;
    transition: 1s ease-out;
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
      linguagens: ['Laravel', 'Vue.js', 'PHP', 'CSS' , 'Javascript', 'Node.js', 'Quasar', 'Bootstrap', 'Vuetify', 'Postgree', 'MySQL', 'React.js', 'Python', 'Tailwind'],
      sk: [{name : 'Laravel', image: 'skils/laravel.png' , color: 'color: #ff2d20;'}, 
            {name: 'Vue.js', image: 'skils/vue.png' , color: 'color: #41b883 ;'}, 
            {name: 'PHP', image: 'skils/php.png' , color: 'color: #778bc7 ;'}, 
            {name: 'CSS', image: 'skils/css.png' , color: 'color: #0089ca;'} , 
            {name: 'Javascript', image: 'skils/js.png' , color: 'color: #f7df1e ;'}, 
            {name: 'Node.js', image: 'skils/node.png' , color: 'color: #80bd00;'}, 
            {name: 'Quasar', image: 'skils/quasar.png' , color: 'color:transparent; background:  conic-gradient( white 180deg, #00b4ff 240deg );-webkit-background-clip: text; background-clip: text;'}, 
            {name: 'Bootstrap', image: 'skils/bootstrap.png' , color: 'color: #5e2aaa;'}, 
            {name: 'Vuetify', image: 'skils/vuetify.png' , color: 'color:transparent; background:  conic-gradient( #1867c0 180deg, #7bc6ff 240deg );-webkit-background-clip: text; background-clip: text;'}, 
            {name: 'Postgre', image: 'skils/Postgre.png' , color: 'color: #346993;'}, 
            {name: 'MySQL', image: 'skils/mysql.png' , color: 'color:transparent; background:  conic-gradient( orange 246deg, #00758f  240deg );-webkit-background-clip: text; background-clip: text;'}, 
            {name: 'React.js', image: 'skils/react.png' , color: 'color: #00dbfc;'}, 
            {name: 'Python', image: 'skils/python.png' , color: 'color:transparent; background:  conic-gradient( yellow 180deg, #346993 240deg );-webkit-background-clip: text; background-clip: text;'}, 
            {name: 'Tailwind', image: 'skils/tailwind.png' , color: 'color:transparent; background: linear-gradient(to right ,#077c92,#06f6de);-webkit-background-clip: text; background-clip: text;'}],
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