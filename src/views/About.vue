<template>
  <div class="about">
    <h1>This is an about page</h1>
    <ion-img :src="imageSrc"></ion-img>
    <ion-button @click="$router.go(-1)">Back</ion-button>
  </div>
</template>

<script>
export default {
  props: ['imageSrc']
}
</script>
