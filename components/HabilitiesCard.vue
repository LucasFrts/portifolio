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
}
</script>
<style scoped>
.card{
    background-color: #034f77;
    color:#fff;
}
.card-header{
    background-color: transparent;
}
</style>