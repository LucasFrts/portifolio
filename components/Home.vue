<template>
    <div>
        <NavTab/>
        <StyledContainer class="nav-compense">
            <ApresentationCard/>
            <Projetos/>
            <AboutMe/>
        </StyledContainer>
        <Footer/>
    </div>
</template>
<script>
import ApresentationCard from './ApresentationCard.vue';
import AboutMe from './AboutMe.vue';
import Footer from './Footer.vue';
export default {
    components:{
        ApresentationCard,
        AboutMe,
        Footer
    }
}
</script>
<style scoped>
.nav-compense{
    padding-top:4rem;
    padding-bottom: 4rem;
}
</style>