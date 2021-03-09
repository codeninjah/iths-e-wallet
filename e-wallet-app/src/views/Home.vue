<template>
  <div class="home">
      <ol>

        <li> {{testCard}}</li>
        
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
      //chosenCard: 0,
    }
  },
  components: {
    CardComponent,
  },
  methods: {
      actived(index){
        this.position = index;
        console.log(this.position)
        return this.Cards[this.position]
      }
      
    },

  computed: {
    testCard(){
      console.log(this.Cards[this.position]) //undefined
      return this.Cards[this.position]
    }
  }

}
</script>


<style>

</style>
