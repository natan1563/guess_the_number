<template>

    <div>
        <div 
          :class="{
            'danger': type==='danger',
            'white': type==='white',
            'success': type==='success'
            }"
        >{{desc}}</div>
    </div>

</template>


<script>
export default {
 data() {
   return {
      name: 'AlertBox'
   }
 },
 props: {
   type: {
     type: String,
     required: true
   },
   desc: {
     type: String,
     required: true
   }
 }
}
</script>

<style lang="scss" scoped>

  div {
    font-family: 'Inter';
    font-style: normal;
    font-weight: 700;
    font-size: 28px;
    line-height: 34px;
    box-sizing: border-box;
    width: 402px;
    height: 78px;
    left: 516px;
    top: 219px;
    border-radius: 12px;
  }

  .white {
    background: #FFFFFF;
    border: 2px solid #C4C4C4;
    color: #333333;
  }

  .danger {
    color: #FF4D54;
    background: rgba(255, 77, 84, 0.38);
    border: 2px solid #FF4D54;
  }

  .success {
    color: #39CC33;
    background: rgba(57, 204, 51, 0.28);
    border: 2px solid #48A728;
  }



</style>