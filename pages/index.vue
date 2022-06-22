<template>
  <div class="body">
    <div class="container">
    <div class="question">Ты сегодня покормил кота?</div>
    <product_card />
    </div>
  </div>
</template>

<script>
import product_card from '@/components/product_card'

export default {
  components: {
    product_card
  },
  data() {
    return{
      product : [
        {
          class: 'card1',
          name: 'с фуагра',
          nodeTypeString: '10 порций мышь в подарок',
          weight: '0,5 кг'
        },
        {
          class: 'card2',
          name: 'с виагра',
          nodeTypeString: '10 порций мышь в подарок',
          weight: '1 кг'
        }
      ]
    }
  }
}

</script>

<style lang="css">
*{
  padding: 0;
  margin: 0;
}
.body{
  background-image: url("static/Pattern.png");
  width: 100%;
  height: 100vh;

}
.container{
  max-width: 1120px;
  margin: 0 auto;
  position: relative;
}
.question{
  font-size: 36px;
  line-height: 44px;
  text-align: center;
  padding: 36px;
  color: #FFFFFF;
}
</style>
