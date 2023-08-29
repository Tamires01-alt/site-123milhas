<template lang="pug">
div(
  class="q-pa-md" style="max-width: 650px"
)
  q-list(
    class="rounded-borders"
  )
    q-expansion-item(
      v-for="item in items"
      :key="item.id"
      :label="item.label"
      :icon="item.icon"
      expand-separator
      hide-expand-icon
    )
      q-separator(
        dark 
      )
      q-card
        q-card-section
          p {{ item.description1 }}
</template>
    
<script>
import { defineComponent } from 'vue'
export default defineComponent({
  name: 'IndexPage',
  data() {
    return {
      items: [
        {
          label: 'O que é o 123assist?',
          description1: 'O 123assist é o mais novo serviço da 123 para você que busca por mais tranquilidade e segurança em suas viagens. O serviço está disponível em nossa plataforma nas vendas de voos e pacotes nacionais e internacionais. Disponíveis em viagens nacionais e internacionais.',
          icon: "fa-solid fa-1"
        },
        {
          label: 'Por que devo contratar um seguro-viagem e para que serve?',
          description1: ' O  seguro-viagem  ajuda   em   situações  de   imprevistos  que   podem   ocorrer durante a viagem. Com esta proteção, você tem a garantia de atendimento hospitalar, odontológica, farmacêutica e até mesmo durante a viagem em situações relacionadas a sua bagagem e atrasos no voo, etc',
          icon: "fa-solid fa-2"
          
        },
        {
          label: 'O seguro-viagem é obrigatório para qualquer tipo de viagem?',
          description1: 'Em muitos países, principalmente na Europa, existe a obrigatoriedade para a  contratação do seguro-viagem por parte do viajante. Ou seja, é requisito  essencial para você entrar no país.',
          icon: "fa-solid fa-3"
        },
        {
          label: 'O Seguro-Viagem 123assist oferece cobertura para situações de Covid-19?',
          description1: 'Sim, A oferta da cobertura irá depender do plano adquirido pelo segurado. Os  planos disponíveis possuem cobertura no valor de até U$ 10.000 (Dez mil  dólares) para cobertura médica em situações relacionadas a Covid-19.',
          icon: "fa-solid fa-4"
        },
        {
          label: 'Quanto custa e quais são os valores de cobertura do Seguro Viagem?',
          description1: 'O valor do 123assist depende de alguns fatores:',
          icon: "fa-solid fa-5"
        }
      ]
    }
  }
})
</script>
<style lang="scss">
</style>