<template>
    <div class="w-100 pt-5">
        <h4 class="text-light bold sublinhado">Principais linguagens:</h4>
        <div class="d-flex flex-row flex-wrap pt-3 gap-30">
            <Tech v-for="({icon, name}) in languages" :key="name">
                <template v-slot:icon>
                    <fa class='icon' :icon='icon'/>
                </template>
                <template v-slot:body>
                    {{ name }}
                </template>
            </Tech>
        </div>
        <h4 class="text-light bold sublinhado pt-5">Principais frameworks:</h4>
        <div class="d-flex flex-row flex-wrap pt-3 gap-30">
            <Tech v-for="({icon, name}) in frameworks" :key="name">
                <template v-slot:icon>
                    <fa class='icon' :icon='icon'/>
                </template>
                <template v-slot:body>
                    {{ name }}
                </template>
            </Tech>
        </div>
        
    </div>
</template>
<script>
import Tech from './Tech.vue'
export default {
    components:{
        Tech
    },
    data(){
        return{
            languages:[
                {
                    icon:["fab","html5"],
                    name:"HTML"
                },
                {
                    icon:["fab","css3-alt"],
                    name:"CSS"
                },
                {
                    icon:["fab","js"],
                    name:"JavaScript"
                },
                {
                    icon:["fab","php"],
                    name:"PHP"
                },
                {
                    icon:["fab","python"],
                    name:"Python"
                },
                {
                    icon:["fab","java"],
                    name:"Java"
                },
                
            ],
            frameworks:[
                {
                    icon:["fab","vuejs"],
                    name:"Vue"
                },
                {
                    icon:["fab","laravel"],
                    name:"Laravel"
                },
                {
                    icon:"flask",
                    name:"Flask"
                },
                {
                    icon:"mobile",
                    name:"Flutter"
                }
            ]
        }
    }
}
</script>
<style scoped>
.icon{
    font-size: 2rem;
}
.gap-30{
    gap:1rem;
}
</style>