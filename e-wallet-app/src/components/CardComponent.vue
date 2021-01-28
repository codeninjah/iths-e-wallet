

<template>
    <div class="card-body">
        <div>
            <img v-if="vendor == EvilCorp" src="../assets/vendor-evil.svg">
            <img v-else-if="vendor == Bitcoin" src="../assets/vendor-bitcoin.svg">
        </div>
        <!--
        <div v-else-if="vendor == Blockchain"  class="vendor">
            <img src="../assets/vendor-blockchain.svg">
        </div>
        <div v-else-if="vendor == NinjaBank"  class="vendor">
            <img src="../assets/vendor-ninja.svg">
        </div>
        -->
        <div class="chip"><img src="../assets/chip-dark.svg"></div>
        <div class="card-number">{{cardNumber}}</div>
        <div class="name-date">
            <div class="card-holder">{{cardHolder}}</div>
            <div class="expire">{{month}} / {{year}}</div>
        </div>
        <div class="vendor">{{vendor}}</div>
    </div>
</template>


<!--
<template>
    <div class="card-body">
        <div class="vendor"><img src="../assets/vendor-evil.svg"></div>
        <div class="chip"><img src="../assets/chip-dark.svg"></div>
        <div class="card-number">{{NewCard.CardNumber}}</div>
        <div class="name-date">
            <div class="card-holder">{{NewCard.CardHolder}}</div>
            <NewCard />
        </div>
    </div>
</template>
-->



<script>

//import NewCard from '../views/NewCard.vue'


export default {
    props: ['cardHolder', 'cardNumber', 'year', 'month', 'logo', 'chip', 'vendor'],

    /*components: {
        NewCard,
    }*/
}
</script>


<style scoped>
    .card-body {
        background-color: red;
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

    .evil {
        background-color: red;
    }

    .blockchain {
        background-color: purple;
    }

    .bitcoin {
        background-color: orange;
    }

    .ninja {
        background-color: black;
    }

</style>

