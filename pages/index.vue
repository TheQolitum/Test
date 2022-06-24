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
          weight: '0,5 кг',
          description: 'Печень утки разварная с артишоками.'
        },
        {
          class: 'card2',
          name: 'с рыбой',
          nodeTypeString: '40 порций 2 мыши в подарок',
          weight: '2 кг',
          description: 'Головы щучьи с чесноком да свежайшая сёмгушка.'
        },
        {
          class: 'card2',
          name: 'с курой',
          nodeTypeString: '100 порций 5 мышей в подарок',
          weight: '5 кг',
          description: 'Филе из цыплят с трюфелями в бульоне.'
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
  max-width: 1920px;
  height: 100vh;
}
.container{
  max-width: 1120px;
  margin: 0 auto;
  position: relative;
}
@media (max-width: 1920px) {
  .container{
    max-width: 1440px;
  }
}
@media (max-width: 1500px) {
  .container{
    max-width: 1200px;
  }
}
@media (max-width: 1280px) {
  .container{
    max-width: 970px;
  }
}
@media (max-width: 992px) {
  .container{
    max-width: 750px;
  }
}
@media (max-width: 767px) {
  .container{
    max-width: none;
  }
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
  flex-wrap: wrap;
  flex: 0 0 33.333%;
}
</style>
