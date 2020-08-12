<template>
  <header class="header">
    <div class="header__wrapper">
      <NavBar />
    </div>
  </header>
</template>

<script>
import NavBar from './NavBar'

export default {
  name: 'TheHeader',
  components: {
    NavBar
  }
}
</script>

<style lang="scss">
  .header{

    &__wrapper{
      @include wrapper;
    }
  }
</style>
