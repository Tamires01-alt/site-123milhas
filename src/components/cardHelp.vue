<template lang="pug">
div(
  class = ""
  )
  q-card(
    class = "my-card2"
    )
    q-card-section(
      horizontal
    )
      q-card-section(
        class=""
      )
        img(
          src="../img/mais-ajuda.png" class="img"
        )
      q-card-section.row(
        class=""
      )
        div(
            class=" title"
        ) Você precisa de mais ajuda?
        button(
          class=" text-xs  text-white"
        ) Preencha um formulário clicando aqui e receba retorno ágil em seu e-mail.
</template>

<script>
import { defineComponent } from 'vue'
export default defineComponent({
  name: 'CardHelp'
})
</script>
<style lang="scss">

.my-card2{
  max-width:700px;
  max-height:80px;
  background-color:#f6993f;
}
.title{
  color: #fff;
  font-size: 18px;
  font-style: normal;
  font-weight: 700;
  line-height: 20px;
  text-align: center;
}
@media screen and (max-width: 700px) {
  .img{
    height: 50px;
    width: 80px;
  }
}
</style>