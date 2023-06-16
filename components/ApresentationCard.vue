<template>
    <div class="row mb-5 pb-5 pt-5">
        <div class="d-md-flex d-none align-items-center col col-md-6 col-12">
            <div class="w-100 bolder text-white">
                <div class="w-100 apresentation text-blue f-15rem">
                        OI<img src="images/hi.gif" class="gif" alt="gif animado">, EU SOU O <span class="text-white">LUCAS!</span>
                </div>
                <div class="w-100 text-ligth f-5rem">
                    <div class="w-100">
                        FULLSTACK
                    </div>
                    <div class="w-100">
                        DEVELOPER
                    </div>
                </div>
                <div class="d-flex justify-content-between pt-3 w-100 gap-30">
                    <b-button class="flex-grow" variant="light">COMEÇAR</b-button>
                    <b-button class="flex-grow btn-blue">CONTATE-ME</b-button>
                </div>
            </div>
        </div>
        <div class="col col-12 d-md-none d-sm-block order-2">
            <div class="w-100 bolder text-white">
                <div class="w-100 apresentation text-blue f-15rem">
                        OI<img src="images/hi.gif" class="gif" alt="gif animado">, EU SOU O <span class="text-blue">LUCAS</span>!
                </div>
                <div class="w-100 text-ligth f-5rem">
                    <div class="w-100">
                        FULLSTACK
                    </div>
                    <div class="w-100">
                        DEVELOPER
                    </div>
                </div>
                <div class="d-flex justify-content-between pt-3 w-100 gap-30">
                    <b-button class="flex-grow" variant="light">COMEÇAR</b-button>
                    <b-button class="flex-grow btn-blue">CONTATE-ME</b-button>
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
    font-size: 2.5vw;
}
.f-5rem{
    font-size: 7vw;
    line-height: 6vw;
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
    height: 2rem;
}
.text-blue{
    color: #034f77 !important;
}
.btn-blue{
    background-color: #034f77 !important;
    color:#fff !important;
    border: 1px solid #034f77;

}
@media (max-width:660px){
    .gif{
        height: 6vw;
    }
    .f-15rem{
        font-size: 6vw;
    }
    .f-5rem{
        font-size: 15vw;
        line-height: 12vw;
        margin: 0 !important;
    }
}
@media(min-width:660px) and (max-width:767px){
    .f-15rem{
    font-size: 4vw;
    }
    .f-5rem{
        font-size: 15vw;
        line-height: 12vw;
        margin: 0 !important;
    }
.gif{
    height: 3rem;
}
}
</style>