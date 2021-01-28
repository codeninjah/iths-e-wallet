<template>
    <div class="form">
        <form>
            <label for="card-nr">CARD NUMBER</label>
            <br />
            <input type="text" id="card-nr" maxlength="10" placeholder="XXXX XXXX XXXX XXXX">
            <br />
            <br />
            <label for="name">CARDHOLDER NAME</label>
            <br />
            <input type="text" id="name" placeholder="Firstname Lastname">
            <br />
            <br />
            <label>MONTH</label>
            <label>YEAR</label>
            <br />
            <input type="text" placeholder="mtest">
            <input type="text" placeholder="ytest">
            <br />
            <br />
            <label>VENDOR</label>
            <br />
            <input type="text" placdeholder="vendor">
            <br />
            <br />
            <input type="submit" id="submit" value="ADD CARD">
        </form>
    </div>
</template>


<script>
export default {
    data(){
        return {
            userinput: "Alex",
        }
    }
}
</script>



<style scoped>

    form {
        margin-left: 300px;
        text-align: left;
    }

    #card-nr {
        width: 380px;
        border: 2px solid black;
        border-radius: 5px;
        font-size: 20px;
        height: 40px;
        padding-left: 15px;
    }

    #name {
        width: 380px;
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
    }

</style>