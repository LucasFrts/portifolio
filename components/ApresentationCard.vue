<template>
    <div class="d-flex w-100 justify-content-center">
        <div class="d-flex align-items-center col-md-6">
            <div class="d-flex align-items-start flex-column bolder text-white">
                <div class="d-flex apresentation weak-white">
                    <h5 class="f-15rem">OI</h5><img src="/images/hi.gif" height="56px" alt="gif animado"><h5 class="f-15rem">, EU SOU O LUCAS!</h5>
                </div>
                <h1 class="f-5rem">FULLSTACK</h1>
                <h1 class="f-5rem">DEVELOPER</h1>
                <div class="d-flex justify-content-between pt-3 w-100 gap-30">
                    <b-button class="flex-grow" variant="light">COMEÇAR</b-button>
                    <b-button class="flex-grow" variant="dark">CONTATE-ME</b-button>
                </div>
            </div>
        </div>
        <div class="col-md-6">
            <img src="/images/person.png" class="img-fluid" alt="cartoon image">
        </div>
    </div>
</template>
<script>
export default {
    
}
</script>
<style scoped>
.apresentation{
    line-height: 1rem;
    align-items: flex-end;
}
.apresentation h5{
    margin:0 !important;
    text-indent: 5px;
}
.bolder h1,h5{
    font-weight: bolder;
}
.f-15rem{
    font-size: 1.5rem;
}
.f-5rem{
    font-size: 5rem;
    line-height: 4rem;
    margin: 0 !important;
}
img{
    z-index:99;
}
.gap-30{
    gap:30px
}
.flex-grow{
    flex-grow: 1;
}
.weak-white{
    color:  #ffffffa6;
}
</style>