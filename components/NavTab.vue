<template>
    <div>
        <b-navbar class="w-100 navbar-ajust" toggleable="lg" id="navbar">
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
            <CodeTag/>
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
import StyledContainer from './StyledContainer.vue';
export default {
    components:{
        StyledContainer
    },
    mounted(){
        window.addEventListener('scroll', function() {
          const navbar = document.getElementById('navbar');
          const scrollPosition = window.pageYOffset || document.documentElement.scrollTop;

          if (scrollPosition > 50) { // Defina a quantidade de scroll que define a mudança de cor
            navbar.classList.add('scrolled');
          } else {
            navbar.classList.remove('scrolled');
          }
        });
    }
}
</script>
<style scoped>
.navbar-ajust{
    position:fixed;
    height: 3.5rem;
    background-color: #00000000;
    z-index: 99999;
    transition: background-color 0.2s ease;
}
.scrolled{
    background-color: #030c2e;
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