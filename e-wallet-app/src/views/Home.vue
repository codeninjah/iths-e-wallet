<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App"/>

    <card-component
      cardNumber="234555"
      cardHolder="Alex"
      month="10"
      year="2023" />


  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'
import CardComponent from '@/components/CardComponent.vue'

export default {

  data() {
    return{
      name: 'Home',
    }
  },
  components: {
    //HelloWorld,
    CardComponent,

  }
}
</script>


<style>

</style>
