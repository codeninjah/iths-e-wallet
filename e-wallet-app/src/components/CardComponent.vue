<template>
<div>
    <div class="card-body" 
        v-bind:class="card.vendor" 
        v-on:click="$emit('active')">
        <div class="first-row">
            <p v-if="card.vendor == 'EvilCorp'"><img src="../assets/vendor-evil.svg"></p>
            <p v-else-if="card.vendor == 'Bitcoin'"><img src="../assets/vendor-bitcoin.svg"></p>
            <p v-else-if="card.vendor == 'NinjaBank'"><img src="../assets/vendor-ninja.svg"></p>
            <p v-else-if="card.vendor == 'Blockchain'"><img src="../assets/vendor-blockchain.svg"></p>
            <img src="../assets/chip-dark.svg">
        </div>
 

        <div class="card-holder">{{card.cardName}}</div>

        <div class="card-number">{{card.cardNr}}</div>
        <div class="name-date">
            
            <div class="expire">{{card.month}} / {{card.year}}</div>
        </div>
        <div class="vendor">{{card.vendor}}</div>
    </div>
</div>
</template>


<script>
//import NewCard from '../views/NewCard.vue'

export default {
    data() { return {
        //vendor: "blue"
    }},
    props: ['card', 'index'],
    
    /*
    methods: {

        //HADE TÄNKT BYGGA PÅ FÖR ATT SWISHA KORT VID KNAPPTRYCK PÅ RESP. KORT
        testar(index){
            console.log("ALEX")
            console.log(index)

            //CHANGES BG COLOR ON FIRST IN ARRAY [0]
            const x = document.getElementsByClassName("card-body")[this.index]
            x.style.backgroundColor = "orange"
            console.log("Bitcoin")

            //Här måste jag tänka till
            this.$root.activeCard = this.$root.cardArray[index]
            //console.log(index)
            console.log(this.$root.activeCard)
        },

    }
    */

}
</script>


<style scoped>
    .card-body {
        width: 600px;
        line-height: 3;
        color: white;
        padding: 25px;
        min-height: 300px;
        max-height: 300px;        
        display: flex;
        flex-direction: row;

    }

    .active-card {
        width: 600px;
        line-height: 3;
        color: white;
        padding: 25px;
        display: flex;
        flex-direction: row;
    }

    /*
    .vendor {
        justify-content: flex-end;
        align-items: flex-start;
    }
    */

    .EvilCorp {
        background-color: red !important;
        border-radius: 20px;
        color: white;
    }

    .Blockchain {
        background-color: purple !important;
        border-radius: 20px;
        color: white;
    }

    .Bitcoin {
        background-color: orange !important;
        border-radius: 20px;
        color: black;
        font-weight: 400;
    }

    .NinjaBank {
        background-color: black !important;
        border-radius: 20px;
        color: white;
    }

    .card-number {
        font-size: 26px;
    }

    .first-row {
        flex-direction: row;
    }

</style>

