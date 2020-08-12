<template>
  <div class="wrapper">
    <div class="inner">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContainerInner',
  data () {
    return {
    }
  }
}
</script>

<style lang="scss" scoped>

  .inner{
    @include media("small-medium"){
      // max-width: 60rem;
      // margin: 0 auto;
    }
    @include media("large"){
      // max-width: 100rem;
      // margin: 0 auto;
    }
  }
</style>
