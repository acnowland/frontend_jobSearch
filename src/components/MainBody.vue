<template>
    <div class="w-flex fill-width mr5 column align-center">
        <w-button class="mt5" bg-color="primary" dark @click="showOverlay = true">
            Add New Job Posting
        </w-button>
        <CardContainer class="ma10"/> 
        <w-overlay
            
            v-model="showOverlay"
            :persistent="persistent"
            :persistent-no-animation="persistentNoAnimation"
            :opacity="opacity">
                <w-button
                    bg-color="primary"
                    lg
                    dark
                    @click="showOverlay = false">
                    <w-icon class="mr2">wi-cross</w-icon>
                    Submit New Job
                </w-button>
        </w-overlay>
    </div>

    
</template>

<script>
import CardContainer from './CardContainer.vue'


export default {
    name: 'MainBody',
    components:{
        CardContainer,

    },
    data: () => ({
  showOverlay: false,
  opacity: 0.6,
  persistent: true,
  persistentNoAnimation: true
})
    
}
</script>


<style scoped>

</style>