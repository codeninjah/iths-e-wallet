<template>
  <div class="home">
      <ol>

        <li> {{actived}} </li>
        
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
        return this.position
      }
      
    },

  computed: {
  }

}
</script>


<style>

</style>
