<template>
  <q-layout view="hHh Lpr lff" container style="height: 700px; background: black; " class="shadow-2 " >
     <q-header elevated class="bg-black" style="    position: fixed;
    width: 100%;
    padding: 15px 0;
    font-family: Ubuntu,sans-serif;
    z-index: 999;
    transition: all .5s ease;">
       <q-toolbar>
         
         <q-toolbar-title style="
    color: #fff;
    font-size: 35px;
    font-weight: 600;
    padding-left: 13%;
"><span style="color: #00ffff;">Dev</span><span>GBR</span></q-toolbar-title>
         <q-btn flat @click="drawerRight = !drawerRight" round dense icon="menu" style="
    margin-right: 3%;
"/>
       </q-toolbar>
     </q-header>
     
     

     <q-page-container style="padding-top: 83px;">
       <q-page padding style="min-height: 817px;">
        <img src="img/bannert.png" style="width: 100%; position: absolute;" alt="">
        <slot style="position: fixed"/>
       </q-page>
     </q-page-container>
   </q-layout>
 
</template>

<style scoped>


</style>

<script>
import { ref } from 'vue'

export default {
 setup () {
   return {
     drawerLeft: ref(false),
     drawerRight: ref(false)
   }
 }
}

  
   

</script>

