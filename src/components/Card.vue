<template>
<w-card class="ma10 card xs-d-flex xs-column">
  <div>
      <h3 class="ml5">Junior Engineer - LinkedIn</h3>
  </div>
  <template #actions>
    <h5 class="ml5">Javascript, Redux, React</h5>
    <div class="spacer"></div>
        <w-button bg-color="primary" dark @click="showOverlay = true">
            Learn More
        </w-button>
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
                    Close
                </w-button>
        </w-overlay>
  </template>
</w-card>


</template>

<script>
export default {
    name: 'Card',
    data: () => ({
  showOverlay: false,
  opacity: 0.6,
  persistent: true,
  persistentNoAnimation: true
})
}
</script>

<style scoped>
.card{
    width:80%
}

</style>