<template>
    <div class="row mb-5 pb-5">
        <div class="d-md-flex d-none align-items-center col col-md-6 col-12">
            <div class="d-flex align-items-start flex-column bolder text-white">
                <div class="d-flex apresentation weak-white">
                    <h5 class="f-15rem">OI</h5><img src="images/hi.gif" class="gif" alt="gif animado"><h5 class="f-15rem">, EU SOU O LUCAS!</h5>
                </div>
                <h1 class="f-5rem">FULLSTACK</h1>
                <h1 class="f-5rem">DEVELOPER</h1>
                <div class="d-flex justify-content-between pt-3 w-100 gap-30">
                    <b-button class="flex-grow" variant="light">COMEÇAR</b-button>
                    <b-button class="flex-grow" variant="dark">CONTATE-ME</b-button>
                </div>
            </div>
        </div>
        <div class="col col-12 d-md-none d-sm-block order-2">
            <div class="d-flex align-items-start flex-column bolder text-white">
                <div class="d-flex apresentation weak-white">
                    <h5 class="f-15rem">OI</h5><img src="images/hi.gif" class="gif" alt="gif animado"><h5 class="f-15rem">, EU SOU O LUCAS!</h5>
                </div>
                <div class="d-flex flex-column text-ligth">
                    <h1 class="f-5rem">FULLSTACK</h1>
                    <h1 class="f-5rem">DEVELOPER</h1>
                </div>
                <div class="d-flex justify-content-between pt-3 w-100 gap-30">
                    <b-button class="flex-grow" variant="light">COMEÇAR</b-button>
                    <b-button class="flex-grow" variant="dark">CONTATE-ME</b-button>
                </div>
            </div>
        </div>
        <div class="col col-md-6 d-none d-md-block order-2">
            <img src="images/person_desktop.png" class="img-fluid" alt="cartoon image">
        </div>
        <div class="col col-12 d-md-none d-sm-block order-1">
            <img src="images/person_mobile.png" class="img-fluid" alt="cartoon image">
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
.gif{
    height: 56px;
}
@media (max-width:576px){
    .gif{
        height: 1.5rem;
    }
    .f-15rem{
        font-size: 1rem;
    }
    .f-5rem{
        font-size: 2.5rem;
        line-height: 2.5rem;
        margin: 0 !important;
    }
}
</style>