<template>
    <div class="pt-5">
        <LeftTransition id="habilities-text" scrolHeight="50">
            <h4 class="text-light bold sublinhado">Projetos pessoais: </h4>
        </LeftTransition>
        <TopTransition  v-for="({name, text, src, img, ms}, index) in projects" scrolHeight="50" :ms="ms" :id="`project-row-${index + 1}`" :key="name">
            <ProjectCard>
                <template v-slot:infos>
                    <div class="w-100 d-flex flex-column align-items-center">
                        <h3 class="bolder">{{ name }}</h3>
                        <div v-html="text" class="pb-5"></div>
                        <a :href="src" target="__blank" class="btn-primary btn btn-blue">ACESSAR</a>
                    </div>
                    
                </template>
                <template v-slot:image>
                    <img :src="img" alt="img project" :ref="`${name}-image`" class="img-fluid">
                </template>
            </ProjectCard>
        </TopTransition>

    </div>
</template>
<script>
import ProjectCard from './ProjectCard.vue';
import LeftTransition from './LeftTransition.vue';
import TopTransition from './TopTransition.vue';
export default {
    components:{
        ProjectCard,
        LeftTransition,
        TopTransition
    },
    data(){
        return{
            projects:[{name:'Palleteria', text:'<p style="margin-bottom:5px;">Projeto de landing page desenvolvida inicialmente em: </p> <p> Laravel + VueJs + Bootstrap e posteriormente migrada para NuxtJs com BootstrapVue </p>', src:"https://lucasfrts.github.io/Palleteria/", img:"images/pallets.png", mobile:"images/pallets_mobile.png", ms: 200}]
        }
    },
    methods:{
        verificarTamanhoTela(){
            const larguraTela = window.innerWidth || document.documentElement.clientWidth;
            this.changeImageProject(larguraTela <= 767);
        },
        changeImageProject(mobile){
            this.projects.forEach((project)=>{
                const image = this.$refs[`${project.name}-image`][0]

                mobile ? image.src = project.mobile : image.src = project.img
            })
        }
    },
    mounted(){
        window.addEventListener('resize', this.verificarTamanhoTela);
        window.addEventListener('load', this.verificarTamanhoTela);
    },
    beforeDestroy(){
        window.removeEventListener('resize', this.verificarTamanhoTela)
        window.removeEventListener('load', this.verificarTamanhoTela);
    }

}
</script>
<style scoped>
.btn-blue{
    background-color: #034f77 !important;
    color:#fff !important;
    border: 1px solid #034f77;
    width: 100%;
    max-width: 250px;
}
.bolder{
    font-weight: bolder;
}
</style>