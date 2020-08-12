<template>
  <ContainerInner class="intro">
    <div class="background" ref="vantaRef"></div>
  </ContainerInner>

</template>

<script>
import ContainerInner from '@components/ContainerInner'
// import { wait } from '@helpers/time'
import * as Three from 'vanta/vendor/three.r95.min.js'
import BIRDS from 'vanta/src/vanta.birds'
window.THREE = Three

export default {
  name: 'TheIntro',
  components: {
    ContainerInner
  },
  data: () => {
    return {
      vantaEffect: null
    }
  },
  created () {
  },
  mounted () {
    this.vantaEffect = BIRDS({
      el: this.$refs.vantaRef,
      mouseControls: true,
      touchControls: true,
      minHeight: 200.00,
      minWidth: 200.00,
      scale: 1.00,
      scaleMobile: 1.00,
      backgroundColor: 0xf9f3ee,
      color1: 0x7936a7,
      color2: 0x73c7d9,
      speedLimit: 6.00,
      THREE: Three
    })
  }

}
</script>

<style scoped>

.background{
position: relative;
height: 85vh;
object-fit: contain;
}

</style>
