<template>

  <div>
    <h2>Em qual número eu estou pensando?</h2>
    <AlertBox type="danger" desc="Você só tem mais 1 jogada!"/>
    <div class="numbers">
      <button v-for="number in 50" v-bind:key="number">{{ number }}</button>
    </div>
  </div>

</template>

<script>
import AlertBox from '@/components/alerts/AlertBox.vue'

export default {
  name: 'App',
  data() {
    return {
      
    }
  },
  components: {
    AlertBox,
  }
}
</script>

<style lang="scss" scoped>

h2 {
    width: 827px;
    height: 56px;
    font-family: 'Inter';
    font-style: normal;
    font-weight: 700;
    font-size: 46px;
    line-height: 56px;
    color: #D84E41;
    margin-bottom: 15px;
}

.numbers {
  margin-bottom: 40px;
}

button {
  font-size: 90px;
}

</style>