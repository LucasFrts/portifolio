<template>
    <div>
        <NavTab/>
        <StyledContainer class="nav-compense">
            <ApresentationCard/>
            <Projetos/>
            <AboutMe/>
        </StyledContainer>
    </div>
</template>
<script>
import ApresentationCard from './ApresentationCard.vue';
import AboutMe from './AboutMe.vue';
export default {
    components:{
        ApresentationCard,
        AboutMe
    }
}
</script>
<style scoped>
.nav-compense{
    padding-top:4rem;
}
</style>