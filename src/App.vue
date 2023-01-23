<template>
  <div id="app">
    <img class='flag' alt="Vue logo" src="./assets/flag.jpeg">
    <h1 class='title'>Spanish Sentence Builder</h1>
    <SpeechPart label="Person" :partList="personList"/>
    <SpeechPart label="Verb" :partList="verbList"/>
    <SpeechPart label="Place" :partList="placeList"/>
    <SpeechPart label="Time" :partList="timeList"/>

  </div>
</template>

<script>
import SpeechPart from './components/SpeechPart.vue'

export default {
  name: 'App',
  components: {
    SpeechPart
  },
  data: function(){
    return {
      personList: ['I', 'You', 'He', 'We'],
      verbList: ['To Eat', 'To Live', 'To Go', 'To Speak', 'To Understand'],
      placeList: ['Restaurant', 'Library', 'Theatre', 'Cinema'],
      timeList: ['Present', 'Past', 'Future']
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 60px;
}

.flag {
  width: 300px;  
}

</style>
