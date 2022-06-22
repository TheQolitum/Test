<template>
  <div class="body">
  <div class="shadow">
    <div class="container">
      <div class="question">Ты сегодня покормил кота?</div>
      <div class="flex">
          <ProductCard
            v-for="(product,key) in products"
            :product="product"
            :key="key" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return{
      products : [
        {
          class: 'card1',
          name: 'с фуагра',
          nodeTypeString: '10 порций мышь в подарок',
          weight: '0,5 кг'
        },
        {
          class: 'card2',
          name: 'с рыбой',
          nodeTypeString: '40 порций 2 мыши в подарок',
          weight: '2 кг'
        },
        {
          class: 'card2',
          name: 'с курой',
          nodeTypeString: '100 порций 5 мышей в подарок',
          weight: '5 кг'
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
.shadow{
  height: 100%;
  background: linear-gradient(180deg, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 5e-05) 49.88%, rgba(0, 0, 0, 0.5) 100%);
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
.flex{
  display: flex;
  justify-content: space-between;
}
</style>
