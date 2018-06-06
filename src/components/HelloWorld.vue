<template>
  <div class="hello">
    漢字：<input type="text" v-model="name" v-on:input="update_furigana">
    ふりがな：<input type="text" v-model="furigana">
  </div>
</template>

<script>
import historykana from 'historykana'

export default {
  name: 'HelloWorld',
  data () {
    return {
      name: '',
      furigana: '',
      history: []
    }
  },
  methods: {
    update_furigana (input) {
      this.history.push(input.target.value)
      this.furigana = historykana(this.history)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
