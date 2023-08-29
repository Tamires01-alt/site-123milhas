<template lang="pug">
q-page(
  class=""
  style="background-color: #f5f5f5;"
)
  div
    div(
      class="font-semibold text-center text-xl p-9 q-gutter-lg"
    ) Confira as vantagens do Seguro Viagem Descomplicado
      div.row.q-gutter-lg.justify-center.q-pr-lg(
      )
        cardSafe(
        )
    div(
      class="font-semibold text-center text-xl q-gutter-md"
    ) Precisou de ajuda durante a viagem?
      div(
        class="descriptionHelp q-gutter-md"
      ) Nos envie um WhatsApp de qualquer lugar que responderemos imediatamente. Atendimento <br> em português, 24h por dia, 7 dias por semana!
        div.justify-center(
          class="flex q-pr-md"
        )
          cardHelp(
          )
        div.justify-center(
          class="flex "
        )
          div(
            class="font-semibold  text-xl"
          ) Tem dúvidas sobre nosso seguro viagem? Estamos aqui para explicar tudo!
            div(
              class="descriptionHelp q-pr-sm"
            ) Navegue abaixo pelas dúvidas mais frequentes sobre o seguro viagem 123 assist.
              expansionDoubts(
                class="text-left"
              )
</template>

<script>
import { defineComponent } from 'vue'
import cardSafe from 'components/cardSafe.vue'
import cardHelp from 'components/cardHelp.vue'
import expansionDoubts from 'src/components/expansionDoubts.vue'

export default defineComponent({
  name: 'IndexPage',
  components: {
    cardSafe,
    cardHelp,
    expansionDoubts
  }
})
</script>
<style lang="scss">

.descriptionHelp{
  color: #414042;
  font-size: 17px;
  font-style: normal;
  font-weight: 400;
  line-height: 23px;
}
</style>
