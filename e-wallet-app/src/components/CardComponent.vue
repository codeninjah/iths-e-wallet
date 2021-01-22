

<template>
    <div class="card-body">
        <div class="vendor"><img src="../assets/vendor-evil.svg"></div>
        <div class="chip"><img src="../assets/chip-dark.svg"></div>
        <div class="card-number">{{cardNumber}}</div>
        <div class="name-date">
            <div class="card-holder">{{cardHolder}}</div>
            <div class="expire">{{month}} / {{year}}</div>
        </div>
    </div>
</template>


<script>
export default {
    props: ['cardHolder', 'cardNumber', 'year', 'month', 'logo', 'chip'],
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

</style>

