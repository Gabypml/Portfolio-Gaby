<template>
  <div id="contact">
    <div class="wrapper">
      <div class="inner">
        <div class="contacts">
          <div class="contacts__items">
            <div class="contacts__items__left">
              <p> Contactez-moi</p><span>↓</span>
            </div>
            <div class="contacts__items__right">
               <a href="mailto:Gaby_pombo.monteiro.leonor@hotmail.com?subject=Mail Du Portfolio">Gaby_pombo.monteiro.leonor@hotmail.com</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

</script>

<style lang="scss" scoped>
#contact{
  .wrapper{
    @include wrapper
    .inner{
      @include inner
      .contacts{

        &__items{
           @include media('small'){

            text-align: center;
            font-size: 1.6rem;
          }
          @include media('medium'){

            text-align: center;
            font-size: 2rem;
          }

          font-size: 2.5rem;
          font-weight: lighter;
          text-align:justify;
          color: #2c3e50;
          padding-bottom: 10rem;
          &__left, &__right{
            @include media('small-medium'){
              margin-right: 0rem;
              margin-left: 0rem;
            }
            text-align: center;
            margin-right: 10rem;
            margin-left: 10rem;
          }
          &__left{
            padding-bottom: 2rem;
            padding-top: 2rem;
            border-top: 1px solid white;
            font-weight: lighter;
            span{
              padding-bottom:1rem;
              &:hover{
                cursor:pointer;
                font-weight: bolder;
              }
            }
          }
          &__right{
            padding-top: 2rem;
            padding-bottom: 2rem;
            border-bottom: 1px solid white;
            font-weight: normal;

            a{
              text-decoration: none;
              color: #2c3e50;
              &:hover{
                font-weight: bolder;
              }
            }
          }
        }
      }
    }
  }
}
</style>
