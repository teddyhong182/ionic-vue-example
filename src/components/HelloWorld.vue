<template>
  <div class="hello">
    <ion-label>Label</ion-label>
    <div>
      <ion-button @click="handleClick">Default</ion-button>
    </div>

    <ion-item>
      <ion-label position="floating">Floating Label</ion-label>
      <ion-input :value="myInput" @input="myInput = $event.target.value"></ion-input>
    </ion-item>

    <ion-grid>
      <ion-row>
        <ion-col>
          <div>1 of 3</div>
        </ion-col>
        <ion-col>
          <div>2 of 3</div>
        </ion-col>
        <ion-col>
          <div>3 of 3</div>
        </ion-col>
      </ion-row>
    </ion-grid>

    <!-- List of Text Items -->
    <ion-list>
      <ion-item>
        <ion-label>Pokémon Yellow</ion-label>
      </ion-item>
      <ion-item>
        <ion-label>Mega Man X</ion-label>
      </ion-item>
      <ion-item>
        <ion-label>The Legend of Zelda</ion-label>
      </ion-item>
      <ion-item>
        <ion-label>Pac-Man</ion-label>
      </ion-item>
      <ion-item>
        <ion-label>Super Mario World</ion-label>
      </ion-item>
    </ion-list>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  mounted () {
    axios.get('https://www.reddit.com/r/aww.json?raw_json=1')
      .then(response => {
        console.log(response.data.data.children)
      })
  },
  data () {
    return {
      myInput: ''
    }
  },
  methods: {
    handleClick () {
      alert(this.myInput)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
