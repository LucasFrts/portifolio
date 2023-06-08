<template>
    <div class="pt-5">
        <h4 class="text-light bold sublinhado">O que posso entregar:</h4>
        <div class="d-flex justify-content-center gap-30 pt-5 row">
            <HabilitiesCard class="col col-md-3 col-12" v-for="({title, content, icon}, index) in habilities" :key="index" :title="title" :content="content">
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
        </div>    
    </div>
</template>
<script>
import HabilitiesCard from './HabilitiesCard.vue';
export default {
    components:{
        HabilitiesCard
    },
    data(){
        return{
            habilities:[
                {
                    title:"APLICAÇÕES FRONTEND",
                    icon:"desktop",
                    content:"<ul><li>Desenvolvimento de lading pages</li><li>Sistemas web</li><li>e Consumo de API's.</li></ul>"
                },
                {
                    title:"APLICAÇÕES BACKEND",
                    icon:"code",
                    content:"<ul><li>Desenvolvimento de API's</li><li>Regras de negócios</li><li>e Estruturação de bancos de dados.</li></ul>"
                },
                {
                    title:"APLICAÇÕES MOBILE/DESKTOP",
                    icon:"mobile-screen",
                    content:"<ul><li>Aplicações mobile com Flutter</li><li>e Aplicações desktop com Java Swing.</li></ul>"
                }
            ]
        }
    }
    
}
</script>
<style scoped>
.gap-30{
    gap:30px
}
.icon{
    font-size: 3rem;
}

</style>