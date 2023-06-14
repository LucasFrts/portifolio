<template>
    <div :ref="id" class="opa hide-cards">
        <div class="card">
            <div class="card-header d-flex justify-content-center">
                <slot name="title">
    
                </slot>
            </div>
            <div class="card-body">
            <slot name="content">
    
            </slot>
        </div>
        </div>
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
    mounted(){
        window.addEventListener('scroll', () => {
            const scrollPosition = window.pageYOffset || document.documentElement.scrollTop;
            const card = this.$refs[this.id]
          if (scrollPosition > this.scrolHeight) { 
            setTimeout(()=>{
                card.classList.remove('hide-cards')
            }, this.ms)
          } else {
            setTimeout(()=>{
                card.classList.add('hide-cards')
            }, this.ms)
          }
        });
    }
}
</script>
<style scoped>
.card{
    background-color: #fff;
    color:#034f77;;
}
.card-header{
    background-color: transparent;
}
.opa{
    transition:.5s ease;
}
.hide-cards{
    margin-top:100%
}
@media (max-width:660px){
    .card{
        max-width: 80%;
    }
}
</style>