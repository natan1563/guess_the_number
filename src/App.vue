<template>
  <div id="app" class="container">

    <Header></Header>

    <NumbersBox />

    <div class="center">
      <hr>
    </div>

    <div class="container-buttons center">
      <action-button 
        class="action-btn"
        :type-button="'help'"
      >      

        <template #icon>
          <img src="./assets/icons/help.svg">
        </template>

        <template #text>
          <p>Pedir ajuda</p>
        </template>
      </action-button>
      
      <action-button 
        class="action-btn"
        :type-button="'give'"
      >      

        <template #icon>
          <img src="./assets/icons/help.svg">
        </template>

        <template #text>
          <p>Pedir ajuda</p>
        </template>
      </action-button>  
    </div>    
  </div>
</template>

<script>
import Header from "@/components/Header.vue"
import ActionButton from './components/buttons/ActionsButtons.vue'
import NumbersBox from './components/numbers/NumbersBox.vue'

export default {
  name: 'App',
  components: {
    Header,
    ActionButton,
    NumbersBox
  }
}
</script>

<style>  
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700;900&display=swap');

* {
  margin: 0px;
  padding: 0px;
}

.center {
  display: flex;
  margin-bottom: 40px;
  justify-content: center;
}

hr {
  width: 892px;
  height: 0px;
  border: 3px solid #ECECEC;
}

.container {
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.25);
  background-color: white;
  margin-top: 40px;
  padding-left: 80px;
  padding-right: 80px;
  margin-left: auto;
  margin-right: auto;
  width: 96%;
  max-width: 1200px;
  padding-top: 80px;
  padding-bottom: 80px;
}

</style>
