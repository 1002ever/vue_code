<template>
  <div>
    <h1>메뉴 추천</h1>
    <button @click="pick">오늘의 메뉴는?</button>
    <hr/>
    {{ menu }}
  </div>
</template>

<script>
import _ from 'lodash'

export default {
  data: function () {
    return {
      menus: ['짜장', '고기', '김치찌개', '남다른감자탕', '매드포갈릭',],
      menu: '',
    }
  },
  methods: {
    pick: function () {
      this.menu = _.sample(this.menus)
    }
  }
}
</script>

<style>

</style>