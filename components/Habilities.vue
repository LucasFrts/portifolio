<template>
    <div class="pt-5">
        <LeftTransition id="habilities-text" scrolHeight="100">
            <h4 class="text-light bold sublinhado">O que posso entregar: </h4>
        </LeftTransition>
        <div class="d-flex justify-content-center gap-30 pt-5 row">
            <TopTransition :id="`card-row-${index + 1}`" :ms="ms" v-for="({title, content, icon, ms}, index) in habilities" :key="index" class="col col-md-3 col-12">
                <HabilitiesCard  class="w-100" >
                <template v-slot:title>
                    {{ title }}
                </template>
                <template v-slot:content>
                    <div class="d-flex justify-content-center flex-column align-items-center">
                        <fa class='icon mt-2 mb-5' :icon='icon'/>
                        <div v-html="content"></div>
                    </div>
                </template>
            </HabilitiesCard>
            </TopTransition>
        </div>    
    </div>
</template>
<script>
import LeftTransition from './LeftTransition.vue';
import HabilitiesCard from './HabilitiesCard.vue';
import TopTransition from './TopTransition.vue';
export default {
    components:{
        HabilitiesCard,
        LeftTransition,
        TopTransition
    },
    data(){
        return{
            habilities:[
                {
                    title:"APLICAÇÕES FRONTEND",
                    icon:"desktop",
                    content:"<ul><li>Desenvolvimento de lading pages</li><li>Sistemas web</li><li>e Consumo de API's.</li></ul>",
                    ms: 200
                },
                {
                    title:"APLICAÇÕES BACKEND",
                    icon:"code",
                    content:"<ul><li>Desenvolvimento de API's</li><li>Regras de negócios</li><li>e Estruturação de bancos de dados.</li></ul>",
                    ms: 400
                },
                {
                    title:"MOBILE/DESKTOP",
                    icon:"mobile-screen",
                    content:"<ul><li>Aplicações mobile com Flutter</li><li>e Aplicações desktop com Java Swing.</li></ul>",
                    ms: 600
                }
            ]
        }
    },

    
}
</script>
<style scoped>
.gap-30{
    gap:30px
}
.icon{
    font-size: 3rem;
}
.hide-text{
    margin-left: -100%;
}
.hide-cards{
    margin-top:100%
}
</style>