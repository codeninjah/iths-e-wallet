<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>

    <Card />
    <Cardform />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Card from '@/components/Card.vue'
import Cardform from '@/components/Cardform.vue'

export default {

  data() {
    return{
      name: 'Home',
    }
  },
  components: {
    HelloWorld,
    Card,
    Cardform
  }
}
</script>


<style>

</style>
