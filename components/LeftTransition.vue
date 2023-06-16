<template>
    <div :ref="id" class="opa hide-text">
    <slot>

    </slot>
    </div>
</template>
<script>
export default {
    props:{
        id:{
            type:String,
            default:""
        },
        scrolHeight:{
            type:String|Number,
            default:"100"
        },
        ms:{
            type:Number,
            default:0
        }
    },
    methods:{
        scrollEvent(){
            const text = this.$refs[this.id];
            const scrollPosition = window.pageYOffset || document.documentElement.scrollTop;     
          if (scrollPosition > this.scrolHeight) { 
            if(text.classList.contains('hide-text')){
                setTimeout(()=>{
                text.classList.remove('hide-text');
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
.hide-text{
    margin-left: -100%;
}
.opa{
    transition: .9s ease;
}
</style>