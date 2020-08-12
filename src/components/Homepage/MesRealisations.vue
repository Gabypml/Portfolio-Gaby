<template>
<div id="MesRealisations">
  <div class="realisations">
    <div class="realisations__wrapper">
      <div class="realisations__wrapper__inner">
        <div class="realisations__wrapper__inner__items">
            <div class="realisations__wrapper__inner__items__mockup">
            <a class="realisations" href="https://gabypml.github.io/Mon_CV/"> <img src="@/assets/CV.jpg" alt="CV"></a>
            <a class="realisations" href="https://debourgeo.github.io/restaurant-css-framework/"><img src="@/assets/ATable_mock.jpg" alt="Site resto"></a>
            <a class="realisations" href="https://github.com/Gabypml"> <img src="@/assets/git.jpg" alt="Compte Github"></a>
            </div>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'MesRealisations',
  data: () => {
    return {
      items: [
        { image: 'CV.jpg', link: 'https://gabypml.github.io/Mon_CV/' },
        { image: 'ATable_mock.jpg', link: 'https://debourgeo.github.io/restaurant-css-framework/' },
        { image: 'git.jpg', link: 'https://github.com/Gabypml' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.realisations{
  &__wrapper{
      @include wrapper;
      &__inner{
        @include inner;
        &__items{
          &__mockup{
            @include media('small-medium'){
              display:initial;
            }
            margin-top:-7rem;
            padding-bottom: 5rem;
            display: flex;
            align-items: center;
            img{
              @include media('small-medium'){
              margin-top: 5rem;
              }
              transition: transform .5s ease;
              &:hover{
                transform: scale(1.1);
              }
            }
            .realisations{
              padding-right: 3rem;
            }
          }
        }
      }
    }
}

</style>
