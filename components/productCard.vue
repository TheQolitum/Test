<template>
  <div>
    <div class="block">
    <div class="card">
  <div class="c_body">
    <div :class="product.class"></div>
  <div class="slog">Сказочное заморское яство</div>
    <div class="company">Нямушка</div>
    <div class="tasty">{{product.name}}</div>
    <div class="stock">{{product.nodeTypeString}}</div>
    <div class="cat"></div>
    <div class="tex">{{product.weight}}</div>
  </div>

      <div class="change">
        <div class="text">
          <p>Что сидишь? Порадуй котэ, <span class="buy">купи</span><span class="memepoint">.</span></p>
        </div>
        <div class="text_hover">
          <p>{{product.description}}</p>
        </div>
    </div>

    </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "productCard",
  props: ["product"]
}
</script>

<style lang="css">
.card{
  width: 320px;
  height: 509px;
  position: relative;
}
.c_body{
  width: 320px;
  height: 472px;
  background-color: white;
  border: 4px solid #1698D9;
  position: relative;
  border-radius: 12px;
}
/*.c_body:hover {*/
/*  border: 4px solid #E52E7A;*/
/*}*/
/*.c_body:hover .tex{*/
/*  background-color: #E52E7A;*/
/*}*/
.slog{
  position: absolute;
  height: 19px;
  left: 15.94%;
  right: 20%;
  top: 21px;

  font-style: normal;
  /*font-weight: 400;*/
  font-size: 16px;
  line-height: 19px;
  color: #666666;
}
.company{
  position: absolute;
  height: 56px;
  left: 15%;
  right: 19.06%;
  top: 36px;

  font-style: normal;
  font-weight: 700;
  font-size: 48px;
  line-height: 56px;
  color: #000000;
}
.tasty{
  position: absolute;
  height: 28px;
  left: 15.94%;
  right: 49.06%;
  top: 90px;

  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 28px;

  color: #000000;
}
.stock{
  position: absolute;
  height: 32px;
  left: 15.94%;
  width: 105px;
  /*right: 50.94%;*/
  top: 125px;

  font-style: normal;
  font-weight: 700;
  font-size: 14px;
  line-height: 16px;

  color: #666666;
}
.cat{
  background-image: url("static/Card/Photo.png");
  bottom: 0;
  position: absolute;
  background-repeat: no-repeat;
  max-width: 320px;
  max-height: 272px;
  width: 100%;
  height: 100%;
  border-radius: 8px;
}
.tex{
  position: absolute;
  padding: 21px;
  width: 58px;
  bottom: 16px;
  right: 16px;
  font-style: normal;
  /* font-weight: 400; */
  font-size: 42px;
  line-height: 30px;
  text-align: center;
  /* color: #FFFFFF; */
  background-color: #1698D9;
  border-radius: 50%;
  color: #FFFFFF;
  letter-spacing: 3px;
}
.buy{
  color: #1698D9;
  text-decoration-line: underline;
  text-decoration-style: dashed;
  text-decoration-color: #1698D9;
}
.memepoint{
  color: #1698D9;
}
.text{
  bottom: 0;
  color: white;
  text-align: center;
  margin: 14px;
  width: 100%;
  overflow:hidden;

}
.text_hover{
  bottom: 0;
  color: white;
  margin: 14px;
  width: 100%;
  overflow:hidden;

}
.block:hover .c_body{
  border: 4px solid #E52E7A;

}
.block:hover .tex{
  background-color: #E52E7A;
}
.change{
  overflow:hidden;
}
.change, .text, .text_hover{
  bottom: 0;
  color: white;
  text-align: center;
}
.text, .text_hover{
  float:left;
  transition: all 0.5s
}
.block:hover .text{
  margin-left:-800px;
}
.text_hover{
  margin-left:-800px;
}
.block:hover .text_hover{
  margin-left:0;
}
</style>
