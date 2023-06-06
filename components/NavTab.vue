<template>
    <div>
        <b-navbar class="w-100 navbar-ajust" toggleable="lg">
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
            <b-collapse id="nav-collapse" is-nav>
                 <b-navbar-nav class="ml-auto mr-5 gap-3 text-white">
                   <b-nav-item class="text-white" href="#">Inicio</b-nav-item>
                   <b-nav-item class="text-white" href="#">Sobre mim</b-nav-item>
                   <b-nav-item class="text-white" href="#">Projetos</b-nav-item>
                   <b-nav-item class="text-white" href="#">Técnologias</b-nav-item>
                 </b-navbar-nav>
            </b-collapse>
        </b-navbar>
    </div>
</template>
<script>
export default {
    
}
</script>
<style scoped>
.navbar-ajust{
    position:fixed;
    height: 3.5rem;
    background-color: #00000000;
}
.gap-3{
    gap:30px
}
.nav-link{
    color: #ffff !important
}
.nav-link:hover{
    background-color: #01013c89;
    border-radius: 5px;
}
</style>