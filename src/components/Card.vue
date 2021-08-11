<template>
<w-card class="ma10 card xs-d-flex xs-column">
  <div>
      <h3 class="ml5">Junior Engineer - LinkedIn</h3>
  </div>
  <template #actions>
    <h5 class="ml5">Javascript, Redux, React</h5>
    <div class="spacer"></div>
        <w-button
        bg-color="primary"
        dark
        @click="showOverlay = true">
        Show a blue overlay
        </w-button>

        <w-overlay
        v-model="showOverlay"
        bg-color="rgba(35, 71, 100, 0.3)"
        :persistent="persistent" :opacity="opacity">
        <div class="hiddenCard">
            <w-card shadow bg-color="white" class="justify-center align-center">
                <h3>Job title here</h3>
                <br><br>
                <p>
                   
                </p>
                <p>Javacript, React, Vue, Node.JS</p>
                <p>8/11/21</p>
            </w-card>
            <w-button
                bg-color="primary"
                lg
                dark
                @click="showOverlay = false"
                class="ma5">
                <w-icon class="mr2">wi-cross</w-icon>
                Hide overlay
            </w-button>
        </div>
        </w-overlay>
  </template>
</w-card>


</template>


<script>


export default {
    name: 'Card',
    data: () => {
        return{
            showOverlay: false,
            opacity: 0.3,
            persistent: true,
        }
    },
}
</script>

<style scoped>
.card{
    width:80%
}
.hiddenCard{
    width: 90%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}
.content {
    display: flex;
}


</style>