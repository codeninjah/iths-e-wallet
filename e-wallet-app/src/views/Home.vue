<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App"/>

    <card-component
      vendor="EvilCorp"
      cardNumber="234555"
      cardHolder="Alex"
      month="10"
      year="2023" />

      <ol>
        <li> {{actived}} </li>

        <li>
          <card-component :card="Cards[this.index]" />
        </li>
        
      <li>
      <card-component v-for="(card, index) in Cards"
        :key="card"
        :index = index
        :card = "Cards[index]" 
        @actived="actived(index)"       
        />
        
        </li>
      </ol>


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
      //byt från c till C
      Cards: this.$root.cardArray,
      active: this.$root.activeCard
    }
  },
  components: {
    //HelloWorld,
    CardComponent,

  },
  methods: {
    
      actived(index){
        this.position = index;
        console.log(this.position)
      }
      
    },

  computed: {
    /*
      Cards(){
        return this.$root.cardArray
      }
      */
  }
}
</script>


<style>

</style>
