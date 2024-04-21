<template>
  <div id="app">
    <h1>Chistes de Chuck Norris</h1>
    <ul>
      <li v-for="(joke, index) in chuck" :key="index" class="joke">
        {{ joke.value }}
      </li>
    </ul>x  x 
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      chuck: [
        {
          "value": "Chuck Norris can skydive into outer space." 
        }, 
        { 
          "value": "The chief export of Chuck Norris is pain." 
        }, 
        { 
          "value": "Chuck Norris doesn't read books. He stares them down until he gets the information he wants." 
        }, 
        { 
          "value": "Time waits for no man. Unless that man is Chuck Norris." 
        }, 
        { 
          "value": "If you spell Chuck Norris in Scrabble, you win. Forever." 
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Arial, sans-serif;
  text-align: center;
  margin-top: 50px;
}

.joke {
  margin: 10px;
  padding: 10px;
  background-color: #f0f0f0;
  border-radius: 5px;
  list-style: none;
}
</style>
