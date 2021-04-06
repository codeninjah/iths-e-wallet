<template>
  <div class="home">
      <ul>

        <li class="active"> <card-component v-bind:card="cards[this.position]" /> </li>

      <li>
      <card-component
        v-for="(card, index) in cards"
        :key="index"
        :card = "cards[index]" 
        @active="active(index)"   
        />
        </li>

      </ul>

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
      position: null,
    }
  },
  components: {
    CardComponent,
  },
  methods: {
      active(index){
        this.position = index;
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


<style scoped>
  .home {
       margin: auto;
       width: 700px;
  }

  ul {
    list-style-type: none;
  }

  .active {
    min-height: 300px;
    max-height: 300px;
  }

  li {
    margin-bottom: 60px;
  }
  
</style>
