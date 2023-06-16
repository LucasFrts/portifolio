<template>
        <div class="card">
            <div class="card-header d-flex justify-content-center">
                <slot name="title">
    
                </slot>
            </div>
            <div class="card-body">
            <slot name="content">
    
            </slot>
        </div>
        </div>
</template>
<script>
export default {
    mounted(){
    }
}
</script>
<style scoped>
.card-body{
    min-height: 280px;
}
.card{
    background-color: #fff;
    color:#034f77;
    margin-left:auto;
    margin-right: auto;
}
.card-header{
    background-color: transparent;
}

@media (max-width:660px){
    .card{
        max-width: 80%;
    }
}
</style>