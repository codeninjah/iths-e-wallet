<template>
    <div class="card-body">
        <div class="card-number">{{cardNumber}}</div>
        <div class="card-holder">{{cardHolder}}</div>
        <div class="expire">{{month}} / {{year}}</div>
    </div>
</template>


<script>
export default {
    props: ['cardHolder', 'cardNumber', 'year', 'month', 'logo', 'chip'],
}
</script>


<style>

</style>