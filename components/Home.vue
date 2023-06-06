<template>
    <div>
        <NavTab/>
        <StyledContainer class="nav-compense">
            <CodeTag/>
        </StyledContainer>
    </div>
</template>
<script>
import StyledContainer from './StyledContainer.vue';
export default {
    components:{
        StyledContainer
    }
}
</script>
<style scoped>
.nav-compense{
    padding-top:4rem;
}
</style>