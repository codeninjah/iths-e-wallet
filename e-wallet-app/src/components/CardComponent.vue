<template>
<div>
    <div class="card-body" 
        v-bind:class="card.vendor" 
        v-on:click="$emit(testar(index))">
        <div>
            <p v-if="card.vendor == 'EvilCorp'"><img src="../assets/vendor-evil.svg"></p>
            <p v-else-if="card.vendor == 'Bitcoin'"><img src="../assets/vendor-bitcoin.svg"></p>
            <p v-else-if="card.vendor == 'NinjaBank'"><img src="../assets/vendor-ninja.svg"></p>
            <p v-else-if="card.vendor == 'Blockchain'"><img src="../assets/vendor-blockchain.svg"></p>
        </div>

        <div class="chip"><img src="../assets/chip-dark.svg"></div>
        <div class="card-number">{{card.cardNumber}}</div>
        <div class="name-date">
            <div class="card-holder">{{card.cardName}}</div>
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
    methods: {

        //HADE TÄNKT BYGGA PÅ FÖR ATT SWISHA KORT VID KNAPPTRYCK PÅ RESP. KORT
        testar(index){
            console.log("ALEX")
            console.log(index)

            //CHANGES BG COLOR ON FIRST IN ARRAY [0]
            const x = document.getElementsByClassName("card-body")[index]
            x.style.backgroundColor = "orange"
            console.log("Bitcoin")

            //Här måste jag tänka till
            this.$root.activeCard = this.$root.cardArray[index]
            //console.log(index)
            console.log(this.$root.activeCard)
        },

    }

}
</script>


<style scoped>
    .card-body {
        width: 670px;
        line-height: 3;
        color: white;
        padding: 25px;
        display: flex;
        flex-direction: column;
    }

    .active-card {
        width: 670px;
        line-height: 3;
        color: white;
        padding: 25px;
        display: flex;
        flex-direction: column;
    }

    .vendor {
        justify-content: flex-end;
        align-items: flex-start;
    }

    .EvilCorp {
        background-color: red !important;
    }

    .Blockchain {
        background-color: purple !important;
    }

    .Bitcoin {
        background-color: orange !important;
    }

    .NinjaBank {
        background-color: black !important;
    }
</style>

