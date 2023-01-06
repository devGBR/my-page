<template>
  <LayoutHome>
    <section class="home" id="home">
      <div class="title" style="position: absolute;">
    <div class="text-1">Olá, meu nome é</div>
    
    <div class="text-2">Gabriel Felipe</div>
   
    <div class="text-3">eu sou <span class="typed-text">{{ typedText }}</span><span class="cursor">&nbsp;</span></div>

    <a class="btn" href="https://drive.google.com/file/d/19c3n8m9d834xtwcWy2c3jJwAMHCi9TvZ/view?usp=sharing">Visualizar CV</a>
  
  </div>
    </section>
  
</LayoutHome>
</template>

<style scoped>
 .btn{
  margin-top: 20px;
  width: 15%;
  height: 10%;
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
    width: 41%;
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
.container p {
  font-size: 3rem;
  padding: 0.5rem;
  font-weight: bold;
  letter-spacing: 0.1rem;
  text-align: center;
  overflow: hidden;
}
 .typed-text {
  font-weight: 600;
  color:  #00ffff;;
}
.container p span.cursor {
  display: inline-block;
  background-color: #ccc;
  margin-left: 0.1rem;
  width: 3px;
  animation: blink 1s infinite;
}
.container p span.cursor.typing {
  animation: none;
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




export default {
  components: { LayoutHome },
  data () {
    return {
      words: ['Full Stack', 'Designer', 'Suporte'],
      typedText: '',
      currentWordIndex: 0,
      currentCharIndex: 0,
      typingSpeed: 100,
      eraseSpeed: 50,
      isErasing: false
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