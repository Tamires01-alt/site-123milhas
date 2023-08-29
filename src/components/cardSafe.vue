<template lang="pug">
div
  div(
    class = "row q-gutter-lg card-desktop"
  )
    q-card(
      v-for="item in items"
        :key="item.id"
        class = "my-card"
      )
      q-card-section.q-col-gutter-lg
        q-icon(
          :name="item.icon"
          size="2.5em"
          color="orange"
        )
        div(
          class="description"
        ) {{ item.description }}
  div(
    class="q-gutter-md card-mobile"
  )
    q-carousel(
      v-model="slide"
      transition-prev="scale"
      transition-next="scale"
      swipeable
      animated
      control-color="dark"
      navigation
      padding
      class="my-card-slide"

    )
      q-carousel-slide(
        :name="slide.name"
        class="column no-wrap flex-center" 
        v-for="slide in items" 
        :key="slide.name"
      )
       
        q-card-section.q-col-gutter-md
          q-icon(
            :name="slide.icon"
            size="2.5em"
            color="orange"
          )
          div(
            class="description"
          ) {{ slide.description }}
</template>

<script>
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'IndexPage',
  data() {
    return {
      items: [
        {
          name: 'one',
          description: 'Orientação medica',
          icon: "fa-solid fa-hospital"
        },
        {
          name: 'two',
          description: 'COVID',
          icon: "fa-solid fa-virus-covid"
        },
        {
          name: 'three',
          description: 'Preços imbativeis',
          icon: "fa-solid fa-tag"
        },
        {
          name: 'four',
          description: '30 serviços e coberturas',
          icon: "fa-solid fa-sheet-plastic"
        }
      ],
      slide: ref('one')
    }
  }
  }
)
</script>
<style lang="scss">
.my-card-slide{
  width:330px;
  height:220px;
  background-color:#fff;
  border: 1px #000 solid;
  margin-left: 3px;
}

.my-card{
  width:170px;
  height:170px;
  background-color:#fff;
  border: 1px #000 solid;
  cursor: pointer;
}
.description{
  color: #414042;
  font-size: 18px;
  font-style: normal;
  font-weight: 700;
  line-height: 20px;
  text-align: center;
}
@media screen and (min-width: 700px) {
  .card-mobile{
    display: none;
    background: none !important;
 }
}
 @media screen and (max-width: 700px) {
  .card-desktop{
    display: none;
  }
}
</style>