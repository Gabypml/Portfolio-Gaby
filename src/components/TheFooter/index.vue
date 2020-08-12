<template>
  <footer class="footer">
    <ContainerInner class="footer__inner"></ContainerInner>
    <MonFooter />
  </footer>
</template>

<script>
import MonFooter from './MonFooter'

export default {
  name: 'TheFooter',
  components: {
    MonFooter
  }
}
</script>

<style lang="scss">
  .footer{}
</style>
