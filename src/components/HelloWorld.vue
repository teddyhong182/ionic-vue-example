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
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data () {
    return {
      myInout: ''
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
