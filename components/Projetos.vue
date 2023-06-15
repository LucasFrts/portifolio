<template>
    <div class="pt-5">
        <ProjectCard v-for="{name, text, src, img} in projects" :key="name">
            <template v-slot:infos>
                <div class="w-100 d-flex flex-column align-items-center">
                    
                    <p>{{ text }}</p>
            <a :href="src" target="__blank" class="btn-primary btn btn-blue">ACESSAR</a>
                </div>
                
            </template>
            <template v-slot:image>
                <img :src="img" alt="img project">
            </template>
        </ProjectCard>
    </div>
</template>
<script>
import ProjectCard from './ProjectCard.vue'
export default {
    components:{
        ProjectCard
    },
    data(){
        return{
            projects:[{name:'Palleteria', text:'Landing page desenvolvida inicialmente em Laravel + VueJs + Bootstrap e depois migrada para NuxtJs com BootstrapVue', src:"https://lucasfrts.github.io/Palleteria/", img:"images/person_desktop.png"}]
        }
    }
}
</script>
<style scoped>
.btn-blue{
    background-color: #034f77 !important;
    color:#fff !important;
    border: 1px solid #034f77;

}
</style>