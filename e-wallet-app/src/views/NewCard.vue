<template>
    <div class="wrapper">
       
            
             <div class="live-card">
                 <!--
                <p>{{ cardNr }}</p>
                <p>{{ cardName }}</p>
                <p>{{ month }}</p>
                <p>{{ year }}</p>
                <p>{{ vendor }}</p>
            -->

                <CardComponent card="card-body"/> 
                 
            </div>   
        
        
    <div class="form">
        <form class="primecard" ref="form">
            <label for="card-nr">CARD NUMBER</label>
            <br />
            <input type="text" name="kortnummer" id="card-nr" maxlength="10" placeholder="XXXX XXXX XXXX XXXX" v-model="cardNr"> 
            <br />
            <br />
            <label for="name">CARDHOLDER NAME</label>
            <br />
            <input type="text" id="name" placeholder="Firstname Lastname" v-model="cardName">
            <br />
            <br />
            <label for="month" id="month-label">MONTH</label>
            <label for="year" id="year-label">YEAR</label>
            <br />
            <select id="month" v-model="month">
                <option value="01">01</option>
                <option value="02">02</option>
                <option value="03">03</option>
                <option value="04">04</option>
                <option value="05">05</option>
                <option value="06">06</option>
                <option value="07">07</option>
                <option value="08">08</option>
                <option value="09">09</option>
                <option value="10">10</option>
                <option value="11">11</option>
                <option value="12">12</option>
            </select>
            <select id="year" v-model="year">
                <option value="20">20</option>
                <option value="21">21</option>
                <option value="22">22</option>
                <option value="23">23</option>
                <option value="24">24</option>
                <option value="25">25</option>
                <option value="26">26</option>
            </select> 
            <br />
            <br />
            <label for="vendor">VENDOR</label>
            <br />

            <select id="vendor" v-model="vendor">
                <option value="Bitcoin">Bitcoin Inc</option>
                <option value="Blockchain">Blockchainn Inc</option>
                <option value="EvilCorp">Evil Corp</option>
                <option value="NinjaBank">Ninja Bank</option>
            </select>

            <br />
            <br />
            <br />
            <br />
            <button id="addCard" v-on:click="addCard()">ADD CARD</button>
            <br />
            <br />
            <router-link to="/">
            <input type="button" id="home" value="BACK TO CARDS">
            </router-link>
        </form>
    </div>
    </div>
</template>


<script>

import CardComponent from "@/components/CardComponent.vue"

export default {

    data(){
        return {
            //userinput: "Alex",
            cardNr: "",
            cardName: "",
            month: "",
            year: "",
            vendor: "",
        }
    },

    components: {
        CardComponent : CardComponent,
    },

    methods: {
        addCard(){       
            this.$root.cardArray.push(
                {cardNr: this.cardNr,
                cardName: this.cardName, 
                month: this.month,
                year: this.year,
                vendor: this.vendor})
            
                this.cardNr = ''
                this.cardName = ''
                this.month = ''
                this.year = ''
                this.vendor = ''

                console.log("TEST")
                //console.log($route.params.slug)
            },

            

        primecard() {
            this.CardComponent.color = "#000000"
            this.CardComponent.cardNr = this.$refs.form.kortnummer.value
            },


            //this.$root.cardArray.push(this.vendor)
            //$this.root hämtar data från main
            //console.log(this.$root.cardArray)
    },

    updated() {
        console.log("Updated")
        console.log(this.cardNr)
        this.CardComponent.this.cardNr = 122918722488472
    },
}

</script>


<style scoped>


    .live-card {
        min-height: 300px;
        max-height: 300px; 
        margin: auto;
    }

    form {
        margin-left: 300px;
        text-align: left;
        width: 380px;
        margin: auto;
    }

    #card-nr {
        width: 360px;
        border: 2px solid black;
        border-radius: 5px;
        font-size: 20px;
        height: 40px;
        padding-left: 15px;
    }

    #name {
        width: 360px;
        border: 2px solid black;
        border-radius: 5px;
        font-size: 20px;
        height: 40px;
        padding-left: 15px;
    }

    #addCard {
        width: 380px;
        height: 50px;
        font-size: 32px;
        border: 2px solid black;
        border-radius: 5px;
        background-color: white;
    }

    #month {
        width: 185px;
        height: 50px;
        font-size: 32px;
        border: 2px solid black;
        border-radius: 5px;
        padding-left: 15px;
    }

    #year-label {
        margin-left: 36%
    }

    #year {
        margin-left: 10px;
        width: 185px;
        height: 50px;
        font-size: 32px;
        border: 2px solid black;
        border-radius: 5px;
        padding-left: 15px;
    }

    #vendor {
        width: 380px;
        height: 50px;
        font-size: 32px;
        border: 2px solid black;
        border-radius: 5px;
        padding-left: 15px;
    }

    #home {
        width: 380px;
        height: 50px;
        font-size: 32px;
        border: 2px solid black;
        border-radius: 5px;
        background-color: white;
    }

    #addCard:hover {
        background-color: grey;
        cursor: pointer;
    }

    #home:hover {
        background-color: grey;
        cursor: pointer;
    }

</style>