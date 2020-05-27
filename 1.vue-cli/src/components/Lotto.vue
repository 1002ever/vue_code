<template>
  <div>
      <h1>로또번호추첨</h1>
      <button @click="pick">추첨</button>
      <p>{{ lucky }}</p>
  </div>
</template>

<script>
// var _ = require('lodash');
import _ from 'lodash'

export default {
    data: function () {
        return {
            numbers: _.range(1,46),
            lucky: '미추첨 상태'
        }
    },
    methods: {
        pick: function () {
            this.lucky = _.sampleSize(this.numbers, 6)
        }
    }
}
</script>

<style>

</style>