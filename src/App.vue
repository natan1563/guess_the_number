<template>
  <div id="app">
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
import ActionButton from './components/buttons/ActionsButtons.vue'
// import AlertBox from '@/components/alerts/AlertBox.vue'

export default {
  name: 'App',
  components: {
    ActionButton,
    // AlertBox
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700;900&display=swap');

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
