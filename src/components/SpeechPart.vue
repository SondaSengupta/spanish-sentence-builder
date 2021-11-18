<template>
  <div>
    <b-button class="button" type="is-primary" @click="getRandomWord">{{label}}</b-button>
    <span class="text">{{this.word}}</span>
  </div>
</template>

<script>
export default {
  name: 'SpeechPart',
  props: {
    label: { required: true, type: String },
    partList: { required: true, type: Array },
  }, 
  data: function () {
    return {
      part: this.partName,
      word: null,
    }
  },
  methods: {
    getRandomWord: function() {
      const randomIndex = Math.floor(Math.random() * this.partList.length);
      const selectedWord = this.partList[randomIndex];
      this.word = selectedWord;
    },
  }
}
</script>
<style>
.button {
  margin: 1rem;
  background-color: pink;
}

.text {
  font-size: 3rem;
  background-color: blue,
}
</style>
