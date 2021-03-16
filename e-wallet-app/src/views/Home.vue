<template>
  <div class="home">
      <ol>

        <li> <card-component v-bind:card="cards[this.position]" /> </li>

      <li>
      <card-component
        v-for="(card, index) in cards"
        :key="index"
        :card = "cards[index]" 
        @active="active(index)"   
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
      //Cards: this.$root.cardArray,
      position: 0,
    }
  },
  components: {
    CardComponent,
  },
  methods: {
      active(index){
        this.position = index;
        //console.log(this.position)
        //return this.Cards[this.position]
      }
      
    },

  computed: {
    cards(){
      console.log("Test card is: ", this.$root.cardArray) //undefined
      return this.$root.cardArray
    }
  }

}
</script>


<style>

</style>
