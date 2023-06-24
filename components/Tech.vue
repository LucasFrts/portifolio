<template>
    <div class="card d-flex flex-row justify-content-center align-items-center gap">
        <div class="card-left">
            <slot name="icon">

            </slot>
        </div>
        <div class="card-right">
            <slot name="body">

            </slot>
        </div>
    </div>
</template>
<script>
export default {
    
}
</script>
<style scoped>
.card{
    padding: .25rem .5rem;
    z-index: 99;
}
.gap{
    gap:10px;
}
.card-left{
    width: fit-content;
    font-size: .9rem;
}
</style>