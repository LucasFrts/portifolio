<template>
    <div>
        <h3 class="bold pl-5">{{ CodeTag }}</h3>
    </div>
</template>
<script>
export default {
    data(){
        return{
            CodeTag:"<LucasFrts/>"
        }
    }
}
</script>
<style scoped>
.bold{
    font-weight: bolder;
    color:#fff;
}
@media(max-width:330px){
    h3{
    display: none; 
    }
}
</style>