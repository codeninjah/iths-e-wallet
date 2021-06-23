<template>
<div>
    <section class="card-body" 
        v-bind:class="card.vendor" 
        v-on:click="$emit('active')">

        <div class="first-row">
            <img class="chip" src="../assets/chip-dark.svg">
                <p v-if="card.vendor == 'EvilCorp'"><img src="../assets/vendor-evil.svg"></p>
                <p v-else-if="card.vendor == 'Bitcoin'"><img src="../assets/vendor-bitcoin.svg"></p>
                <p v-else-if="card.vendor == 'NinjaBank'"><img src="../assets/vendor-ninja.svg"></p>
                <p v-else-if="card.vendor == 'Blockchain'"><img src="../assets/vendor-blockchain.svg"></p>
        </div>
 

        <div class="card-number">{{card.cardNr}}</div>        

        <div class="name-date">
            <div class="name-date-text">
                <div class="name">CARDHOLDER NAME</div>
                <div class="valid">VALID THRU</div>
            </div>
            <div class="name-date-data">
                <div class="card-holder">{{card.cardName}}</div>
                <div class="expire">{{card.month}} / {{card.year}}</div>
            </div>
        </div>

        <!--
        <div class="vendor">{{card.vendor}}</div>
        -->

    </section>
</div>
</template>


<script>
//import NewCard from '../views/NewCard.vue'

export default {
    data() { return {
        //vendor: "blue"
    }},
    props: ['card', 'index'],
    
}
</script>


<style scoped>
    .card-body {
        width: 600px;
        /*line-height: 3;*/
        color: white;
        padding: 25px;
        min-height: 300px;
        max-height: 300px;        
        display: flex;
        flex-direction: column;
        Justify-content: space-between;

    }

    .active-card {
        width: 600px;
        margin-bottom: 100px;
        /*line-height: 3;*/
        color: white;
        padding: 25px;
        display: flex;
        flex-direction: row;
        min-height: 300px;
        max-height: 300px;
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

    .chip {
        align-self: flex-start;
    }

    
    .first-row {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }

    .name-date {
        display: grid;
        /*flex-direction: row;*/
        /*justify-content: space-between;*/
    }
    
    .name-date-text {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }

    .name-date-data {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }


</style>

