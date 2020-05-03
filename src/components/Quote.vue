<template>
<div>
    <h3>{{ quoteSubject }}</h3>
    <p>{{ quoteBody }}</p>
    <button @click="getQuote()">Refresh</button>
</div>
</template>
<script>

import axios from 'axios'

export default {
  name: 'quote',
  data () {
    return {
      quoteBody: '',
      quoteSubject: ''
    }
  },
  methods: {
    getQuote: function () {
      var _this = this

      axios.get('https://api.tronalddump.io/random/quote')
        .then(function (response) {
          console.log(response)
          _this.quoteBody = response.data.value
          _this.quoteSubject = 'Trump on ' + response.data.tags[0]
        })
    }
  },
  mounted: function () {
    this.getQuote()
  }
}
</script>
