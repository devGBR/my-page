<template>
  <LayoutHome>
  <div class="container" style="position: absolute;">
    <p>Me chamo</p>
    
    <p style="font-size:  100px;">Gabriel Felipe</p>
   
    <p>Eu sou <span class="typed-text">{{ typedText }}</span><span class="cursor">&nbsp;</span></p>
  
  </div>
</LayoutHome>
</template>

<style scoped>

.container {
  height: 100vh;
  
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
.container p {
  font-size: 3rem;
  padding: 0.5rem;
  font-weight: bold;
  letter-spacing: 0.1rem;
  text-align: center;
  overflow: hidden;
}
.container p span.typed-text {
  font-weight: normal;
  color: #dd7732;
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
@keyframes blink {
  0%  { background-color: #ccc; }
  49% { background-color: #ccc; }
  50% { background-color: transparent; }
  99% { background-color: transparent; }
  100%  { background-color: #ccc; }
}
</style>

<script>
import LayoutHome from '@/Layout/LayoutHome.vue';




export default {
  components: { LayoutHome },
  data () {
    return {
      words: ['Developer Full Stack', 'Designer', 'Suporte TEC'],
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
    }
  }
}
    


   
    

</script>