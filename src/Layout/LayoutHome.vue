<template>
  <q-layout view="hHh lpR fFf" style=" background: black; " class="shadow-2 ">
     <q-header elevated class="bg-black" style="    position: fixed;
    width: 100%;
    padding: 15px 0;
    font-family: 'Ubuntu',sans-serif;
    z-index: 999;
    transition: all .5s ease;">
       <q-toolbar>
        
         
         <q-toolbar-title style="
    color: #fff;
    font-size: 35px;
    font-weight: 600;
    padding-left: 13%;
"><span style="color: #00ffff;">Dev</span><span>GBR</span></q-toolbar-title>
      <div class="links">
        <a href="#home">Inicio</a>
        <a href="#sobremim">Sobre mim</a>
        <a href="#skils">Skils</a>
        <a href="#exp">Experiências/Cursos</a>
        <a href="#projetos">Projetos</a>
        <a href="#footer">Contato</a>
      </div>
        
        <q-btn flat @click="openNav()" v-if="close===false" round dense icon="menu" class="sidebtn" style="margin-right: 4%;"/>
        <q-btn flat @click="closeNav()" v-if="close===true" round dense icon="close" class="sidebtn" style="margin-right: 4%;"/>
        
       </q-toolbar>
     </q-header>
     <div :style="myside" class="sidenav">
            
            <a href="#">About</a>
            <a href="#">Services</a>
            <a href="#">Clients</a>
            <a href="#">Contact</a>
            
        </div>
     

     <q-page-container style="padding-top: 83px;">
       <q-page  style="min-height: 817px;">
        
        <slot />
        <footer id="footer">
          <q-card  class="my-card">
            <q-card-section>
              <div class="title">
              <div class="text-h6">
                Contato
              </div>
              <div class="barra">
                <div class="falecomigo">
                  Fale Comigo
                </div>
              </div>
            </div>
            <q-card-section>
              
            </q-card-section>
        </q-card-section>
            <q-card-section>
              <div class="cardfoo">
               <div class="textfoo">Criado por <span style="color: #00ffff;">Dev</span><span>GBR</span> | ©Todos os direitos reservado 2023
               </div>
              </div>
            </q-card-section>
          </q-card>
        </footer>
        <div style=" position: fixed; top: 67%; right: 2%;">
        <FloatingActionsVue/>
        </div>
        
       </q-page>
     </q-page-container>
   </q-layout>
 
</template>

<style scoped>
.textfoo{
  color: white;
  margin: 10px auto;
  
  font-size: 17px;
}
.cardfoo{
  border: solid;
    position: absolute;
    /* bottom: 0; */
    left: 0px;
    background: black;
    width: 100.02%;
    height: 50px;
    display: flex;
}
.text-h6{
  margin: 0 auto;
  font-size: 50px !important;
  font-family: 'UbuntuBold', sans-serif;
}
.falecomigo{
    position: absolute;
    top: 57px;
    left: 50%;
    font-size: 20px;
    background: #fff;
    color: #29d8ff;
    padding: 5px;
    transform: translateX(-50%);
}
.title{
    display: flex;
    justify-content: center;
    flex-direction: column;
    
}
.barra{
    width: 180px;
    height: 4px;
    background: rgb(7, 7, 7);
    border: solid;
    margin-top: 30px !important;
    margin: 0 auto;
}
.links{
  margin-right: 40px;
 
}

a{
  text-decoration: none;
  color: white;
  margin-left: 30px;
}
.sidebtn{
  display: none;
  transition: 0.3s;
}
.sidenav {
  height: 100%;
  display: none;
  position: fixed;
  z-index: 1;
  top: 31px;
  left: 0;
  background-color: #111;
  overflow-x: hidden;
  transition: 0.5s;
  padding-top: 60px;
  text-align:center;
}
.sidenav a {
  padding: 8px 8px 8px 32px;
  text-decoration: none;
  font-size: 25px;
  color: #818181;
  display: block;
  transition: 0.3s;

}

.sidenav a:hover{
  color: #f1f1f1;
}

.sidenav .closebtn {
  position: absolute; 
  right: 25px;
  font-size: 36px;
  margin-left: 50px;
}
.closebtn{
  position: fixed;
  top: 10px;
}

@media screen and (max-height: 450px) {
  
  .sidenav a {font-size: 18px;}
}
@media only screen and(max-width: 700px){
  .bg{
      height: 40% !important;
    }
}
@media only screen and (max-width: 864px){
    .sidenav{
      display:block;
    }
    .links{
      display: none;
    }
    .sidebtn{
      display: block;
    }
}

</style>

<script>
import { ref } from 'vue'
import FloatingActionsVue from '@/components/FloatingActions.vue';
export default {
  components: {
    FloatingActionsVue
  },
 data() {
   return {
      drawerLeft: ref(false),
      drawerRight: ref(false),
      myside: "width: 0;",
      close: false,
        }
    },
    methods: {
        openNav(){
            this.myside = "width: 100%; position: fixed;";
            this.close = true;
            console.log(this.myside)
        },
        closeNav(){
          this.myside = "width: 0;";
          this.close = false;
        }
   }
}

  
   

</script>