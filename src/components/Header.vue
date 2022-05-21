<template>
<div>
<h1>
    <strong class="uni">Un1</strong><strong class="games">Games</strong> - Adivinhe o número
</h1>
</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800;900&display=swap');

div {
    text-align: center;
    width: 100%; 
    padding-top: 26px ;
    padding-bottom: 29px;
}

h1{
    font-family: 'Inter';
    text-align: center;
    size: 46px;
}
    .uni{
        color:#D84E41;
    }
    .games{
        color: rgb(245, 87, 30);
    }
</style>
    