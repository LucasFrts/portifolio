<template>
        <div :class="{ 'flex-row-reverse': invert }" class="col col-md-12 d-flex row justify-content-between pt-4">
            <div class="col-md-6">
                <div class="card">
                    <div class="card-body">
                        <slot name="infos">
    
                        </slot>
                    </div>
                </div>
            </div>
            <div class="col-md-6">
                <slot name="image">
    
                </slot>
            </div>
        </div>
</template>
<script>
export default {
    props: {
    invert: {
      type: Boolean,
      default: false,
    },
  },
  mounted(){

    }
}
</script>
<style scoped>
</style>