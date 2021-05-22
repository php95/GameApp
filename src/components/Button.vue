<template>
    <button type="button" class="btn btn-primary">{{text}}</button>
</template>
<script>

export default {
    props:{
        text:String
    }
    
}
</script>
<style scoped>
.btn-primary{
    background-color: #572589;
    border-color :#572589;
    border-radius: 2px;
    width: 100%;
}
</style>

