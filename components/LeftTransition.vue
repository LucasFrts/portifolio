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
    mounted(){
        window.addEventListener('scroll', () => {
            const text = this.$refs[this.id];
            const scrollPosition = window.pageYOffset || document.documentElement.scrollTop;     
          if (scrollPosition > this.scrolHeight) { 
            setTimeout(()=>{
                text.classList.remove('hide-text');
            }, this.ms)
          } else {
            setTimeout(()=>{
                text.classList.add('hide-text');
            }, this.ms)
          }
        });
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