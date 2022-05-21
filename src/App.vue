<template>
  <div id="app">

    <Header></Header>

    <action-button 
      :type-button="'help'"
    >      
      <template #icon>
        <img src="./assets/icons/help.svg">
      </template>

      <template #text>
        <p>Pedir ajuda</p>
      </template>
    </action-button>
    <!-- <AlertBox type="danger" desc="Você só tem mais 1 jogada!"/>
    <AlertBox type="white" desc="Você ainda tem 8 jogadas!"/>
    <AlertBox type="success" desc="Parabéns, você venceu!"/> -->
  </div>
</template>

<script>
import Header from "@/components/Header.vue"
import ActionButton from './components/buttons/ActionsButtons.vue'
// import AlertBox from '@/components/alerts/AlertBox.vue'

export default {
  name: 'App',
  components: {
    Header,
    ActionButton
    // AlertBox
  }
}
</script>

<style>  
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700;900&display=swap');

*{
  margin: 0px;
  padding: 0px;
}
</style>
