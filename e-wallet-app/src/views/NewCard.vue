<template>
    <div class="form">
        <form>
            <label for="card-nr">CARD NUMBER</label>
            <br />
            <input type="text" id="card-nr" maxlength="10" placeholder="XXXX XXXX XXXX XXXX"> {{CardNumber}}
            <br />
            <br />
            <label for="name">CARDHOLDER NAME</label>
            <br />
            <input type="text" id="name" placeholder="Firstname Lastname"> {{CardHolder}}
            <br />
            <br />
            <label for="month" id="month-label">MONTH</label>
            <label for="year" id="year-label">YEAR</label>
            <br />
            <select id="month">
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
            <select id="year">
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

            <select id="vendor">
                <option value="Bitcoin">Bitcoin Inc</option>
                <option value="Blockchain">Blockchainn Inc</option>
                <option value="EvilCorp">Evil Corp</option>
                <option value="NinjaBank">Ninja Bank</option>
            </select>

            <br />
            <br />
            <br />
            <br />
            <input type="submit" id="submit" value="ADD CARD">
            <br />
            <br />
            <router-link to="/"><input type="button" id="home" value="BACK TO CARDS"></router-link>
        </form>
    </div>
</template>


<script>
export default {
    data(){
        return {
            //userinput: "Alex",
        }
    },
    /*props: ["CardNumber",
            "CardHolder", 
            ]*/
}
</script>



<style scoped>

    form {
        margin-left: 300px;
        text-align: left;
        width: 380px;
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

    #submit {
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

    #submit:hover {
        background-color: grey;
        cursor: pointer;
    }

    #home:hover {
        background-color: grey;
        cursor: pointer;
    }

</style>