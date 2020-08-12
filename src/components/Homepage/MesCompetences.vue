<template>
  <div id="MesCompetences">
    <div class="inner">
      <div class="wrapper">
        <div class="anim">
        <div class="logos__item" v-for="logo in logos" :key="logo">
              <div class="logos__item__inner">
                <img alt="logos" class="logos__item__inner__competences" :src="`${publicPath}images/${logo}`">
              </div>
            </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      publicPath: process.env.BASE_URL,
      logos: [
        'HTML5.png',
        'Css3.png',
        'js.png',
        'vuejs.png',
        'git.png'
      ]
    }
  }
}
</script>

<style lang='scss' scoped>
.wrapper{
  background-color: white;

  .anim{
    display:flex;
    align-items: center;
    justify-content: center;
    position: relative;
      margin-top: 10rem;
      margin-bottom: 10rem;
      animation-duration: 5s;
      animation-timing-function: linear;
      animation-name: fadeInOut;
      animation-iteration-count: infinite;
      animation-direction: alternate;
      @keyframes fadeInOut {
       0%{transform:translateX(50px)}
      100%{transform:translateX(-50px)}
      }
  }
  .logos__item{
  position: relative;
  width: 100%;
  overflow: hidden;

  &__inner{
    max-width: 10rem;

    &__competences{
      @include media('small'){
        max-width: 7rem;
      }
      max-width: 15rem;
      padding-top:10rem;
      padding-bottom: 10rem;
    }
  }
}
}
</style>
