<template>
    <div :ref="id" class="opa hide-cards">
        <slot>
            
        </slot>
    </div>
</template>
<script>
export default {
    props:{
        ms:{
            type:Number,
            default: 0
        },
        id:{
            type:String,
            default:""
        },
        scrolHeight:{
            type:String|Number,
            default:"100"
        }
    },  
    methods:{
        scrollEvent(){
            const scrollPosition = window.pageYOffset || document.documentElement.scrollTop;
            const card = this.$refs[this.id]
            if (scrollPosition > this.scrolHeight) { 
              if(card.classList.contains('hide-cards')){
                  setTimeout(()=>{
                      card.classList.remove('hide-cards')
                  }, this.ms)
              }
            }
        }
    },
    mounted(){
        window.addEventListener('scroll', this.scrollEvent);
    },
    beforeDestroy(){
        window.removeEventListener('scroll', this.scrollEvent);
    }
}
</script>
<style scoped>
</style>