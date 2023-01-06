<template>
    <div class="q-px-sm q-py-lg">
    <div class="column items-center" style="margin-top: 100px; margin-bottom: 100px;">
      <q-fab color="purple" icon="keyboard_arrow_up" direction="up">
        <q-fab-action color="primary" @click="onClick" icon="mail" />
        <q-fab-action color="secondary" @click="onClick" icon="alarm" />
      </q-fab>
    </div>
    </div>
</template>
<script>
export default {
  data(){
    return {
      
      }
    },
    methods: {
        onClick(){

        }
    }
  }

</script>