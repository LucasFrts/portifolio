<template>
    <div class="w-100 pt-5">
        <div class="w-100 pt-5">
            <LeftTransition id="princ-ling" scrolHeight="400">
                <h4 class="text-light bold sublinhado">Principais linguagens: </h4>
            </LeftTransition>
            <div class="d-flex flex-row flex-wrap pt-3 gap-30">
                <LeftTransition :id="`lang-${index}`" :ms="150 * (index + 1)" scrolHeight="400"
                    v-for="({ icon, name }, index) in languages" :key="name">
                    <Tech>
                        <template v-slot:icon>
                            <fa class='icon' :icon='icon' />
                        </template>
                        <template v-slot:body>
                            {{ name }}
                        </template>
                    </Tech>
                </LeftTransition>
            </div>
        </div>
        <div class="w-100 pt-5 mt-4">
            <LeftTransition id="princ-fmw" scrolHeight="600">
                <h4 class="text-light bold sublinhado">Principais frameworks: </h4>
            </LeftTransition>
            <div class="d-flex flex-row flex-wrap pt-3 gap-30">
                <LeftTransition :id="`fwm-${index}`" :ms="150 * (index + 1)" scrolHeight="600"
                    v-for="({ icon, name }, index) in frameworks" :key="name">
                    <Tech>
                        <template v-slot:icon>
                            <fa class='icon' :icon='icon' />
                        </template>
                        <template v-slot:body>
                            {{ name }}
                        </template>
                    </Tech>
                </LeftTransition>
            </div>
        </div>
    </div>
</template>
<script>
import Tech from './Tech.vue'
import LeftTransition from './LeftTransition.vue';
export default {
    components: {
        Tech,
        LeftTransition
    },
    data() {
        return {
            languages: [
                {
                    icon: ["fab", "html5"],
                    name: "HTML"
                },
                {
                    icon: ["fab", "css3-alt"],
                    name: "CSS"
                },
                {
                    icon: ["fab", "js"],
                    name: "JavaScript"
                },
                {
                    icon: ["fab", "php"],
                    name: "PHP"
                },
                {
                    icon: ["fab", "python"],
                    name: "Python"
                },
                {
                    icon: ["fab", "java"],
                    name: "Java"
                },

            ],
            frameworks: [
                {
                    icon: ["fab", "vuejs"],
                    name: "Vue"
                },
                {
                    icon: ["fab", "laravel"],
                    name: "Laravel"
                },
                {
                    icon: "flask",
                    name: "Flask"
                },
                {
                    icon: "mobile",
                    name: "Flutter"
                }
            ]
        }
    }
}
</script>
<style scoped>
.icon {
    font-size: 2rem;
}

.gap-30 {
    gap: 1rem;
}
</style>