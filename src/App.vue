<template>
  <div id="app" class="container">

    <Header></Header>

    <action-button 
      :type-button="handdlerHelp"
      v-on:mouseover="help = 'helpHover'"
    >
      <template #icon>
        <img src="./assets/icons/help.svg">
      </template>

      <template #text>
        <p>Pedir ajuda</p>
      </template>
    </action-button>
    
    <action-button 
      :type-button="'give'"
    >      
      <template #icon>
        <img src="./assets/icons/giveUp.svg">
      </template>

      <template #text>
        <p>Desistir</p>
      </template>
    </action-button>

    <action-button 
      :type-button="'disabled'"
    >      
      <template #icon>
        <img src="./assets/icons/help.svg">
      </template>

      <template #text>
        <p>Pedir ajuda</p>
      </template>
    </action-button>

    <action-button 
      :type-button="'again'"
      :widthButton="180"
    >      
      <template #icon>
        <img src="./assets/icons/again.svg">
      </template>

      <template #text>
        <p>Jogar novamente </p>
      </template>
    </action-button> 
    <!-- <AlertBox type="danger" desc="Você só tem mais 1 jogada!"/>
    <AlertBox type="white" desc="Você ainda tem 8 jogadas!"/>
    <AlertBox type="success" desc="Parabéns, você venceu!"/> -->
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
  data() {
    return {
      help: 'help'
    }
  },

  computed: {
    handdlerHelp() {
      console.log('change help for', this.help)
      return this.help 
    }
  },

  methods: {
    handler() {
      console.log('change handler for', this.help)
    }
  },
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
