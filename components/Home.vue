<template>
    <div>
        <NavTab/>
        <StyledContainer class="nav-compense">
            <ApresentationCard/>
        </StyledContainer>
    </div>
</template>
<script>
import ApresentationCard from './ApresentationCard.vue';
export default {
    components:{
        ApresentationCard
    }
}
</script>
<style scoped>
.nav-compense{
    padding-top:4rem;
}
</style>