<template>
  <div class="home">
    <v-container>
      <vue-typed-js :strings="['Python', 'Django', 'Vue', 'Web']" :loop="true" @onComplete="doSmth()">
        <h2>I am a <span class="typing"></span>Developer</h2>
      </vue-typed-js>
      <vue-typed-js :strings="['Web Development', 'Python','Django','System Engineering','Entry Level position','Cloud','AWS','Azure']" :loop="true" @onComplete="doSmth()">
        <h2>Looking for opportunities in <span class="typing"></span></h2>
      </vue-typed-js>
      <br>
      <v-btn href="https://drive.google.com/file/d/174Ti9v24Sn89w3anxgmXVA274pTKhrIF/view?usp=sharing" target="_blank">
      <v-icon>notranslate mdi mdi-file theme--light</v-icon>
        Here's My CV
      </v-btn>
    </v-container>
  </div>
</template>

<script>
import Vue from 'vue'
import VueTypedJs from 'vue-typed-js'

Vue.use(VueTypedJs)

export default {
  name: 'Home',
  components: { }
}
</script>
