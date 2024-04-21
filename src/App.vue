<template>
  <div id="app">
    <div class="container">
      <h1 class="text-center my-4 display-4 title">Chistes de Chuck Norris</h1>
      <div class="row">
        <chuck-card v-for="(joke, index) in chuck" :key="index" :icon-url="joke.icon_url" :value="joke.value"></chuck-card>
      </div>
    </div>
  </div>
</template>

<script>
import ChuckCard from './components/ChuckCard.vue';

export default {
  name: 'App',
  components: {
    ChuckCard
  },
  data() {
    return {
      chuck: [
        {
          "icon_url": "https://img.washingtonpost.com/rf/image_1484w/2010-2019/WashingtonPost/2011/09/27/Style/Images/c92715.jpg?uuid=XjXZeukVEeCWYL6E-yTJeQ",
          "value": "Chuck Norris can skydive into outer space."
        }, 
        { 
          "icon_url": "https://th.bing.com/th/id/R.79ab9413a5faa0f5a0b1c9673ad6128d?rik=e2HQb7lwgqWWUg&riu=http%3a%2f%2fwww.thefamouspeople.com%2fprofiles%2fimages%2fchuck-norris-3.jpg&ehk=J2gLDaD5PFNFgiwioNk4VVyUz9PTtSvh88fp8JqVoZ0%3d&risl=&pid=ImgRaw&r=0",
          "value": "The chief export of Chuck Norris is pain."
        }, 
        { 
          "icon_url": "https://sf2.closermag.fr/wp-content/uploads/closermag/2023/04/chuck-norris-los-angeles-2002-276x410.jpg",
          "value": "Chuck Norris doesn't read books. He stares them down until he gets the information he wants."
        }, 
        { 
          "icon_url": "https://hips.hearstapps.com/hmg-prod/images/gettyimages-150327735-copy.jpg",
          "value": "Time waits for no man. Unless that man is Chuck Norris."
        }, 
        { 
          "icon_url": "https://th.bing.com/th/id/OIP.EcPCdaf4uZU-HWuLHFlkfwHaFP?w=700&h=496&rs=1&pid=ImgDetMain",
          "value": "If you spell Chuck Norris in Scrabble, you win. Forever."
        }
      ]
    }
  }
}
</script>

<style>
#app {
  background-color: #f8f9fa;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.title {
  color: #333;
  font-family: 'Arial', sans-serif;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}
</style>
