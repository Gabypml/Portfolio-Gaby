<template>
<div id="ThePresentation">
  <div class="inner">
    <div class="wrapper">
      <div class="logo">
          <img class="logoKpy" alt="LogoDev" src="@/assets/logoGaby.png" >
      </div>
      <div class="items">
        <div class="items__picture">
          <img class="picture" alt="Portrait-Picture" src="@/assets/gaby.png">
        </div>
        <div class="items__informations">
          <h2> Qui suis-je?</h2>
          <p>Bonjour à tous! <br>
            Fraîchement sortie de stage après ma formation de développeur web,
            je suis activement à la recherche d'un emploi en tant que developpeuse web front-end.
            Durant mon stage j'ai principalement travaillé avec du VueJS et participé a plusieurs projets clients !
            Ayant fait des études artistiques et publicitaires auparavant, j'éprouve plus d'attirance pour ce qui est plus visuel.
            D'où mon penchant pour le Front-end.
            Ma formation aura durer que 10 mois, du coup j'ai encore beaucoup à apprendre. Mais j'ai vraiment beaucoup de motivation !
            Dans tout les cas, c'est un métier où l'on en apprend tous les jours et c'est ce qui me plaît aussi !  </p>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  mounted () {
  }
}
</script>

<style lang='scss' scoped>
#ThePresentation{
  background-color: white;
  .inner{
    @include inner;
    .wrapper{
      @include wrapper;
       @include media('small-medium'){
         padding-bottom: 2rem;
        }
        padding-bottom: 15rem;
      .logo{
        @include media('small-medium'){
         padding-top: 5rem;
          max-width: 75%;
        }
        max-width: 60%;
        margin-left: auto;
        margin-right: auto;
        padding-bottom: 10rem;
        animation: 2s appear;
          @keyframes appear {
            0% {
              opacity: 0;
            }
          }

        .logoKpy{
          border-bottom: 3px solid #f7e7d9;
        }
      }
      .items{
        @include media('small-medium'){
          display: initial;
          padding-bottom: 2rem;
        }
        display: flex;
        padding-bottom: 5rem;
        &__picture{
          margin-right: 2rem;
        }
        &__informations{
          @include media('small-medium'){
            margin-left: 1rem;
            margin-right: 1rem;
            margin-top: 10rem;
            margin-bottom: 10rem;
          }
          margin-left: 5rem;
          line-height: 3.5rem;
          font-weight: 300;
          text-align:justify;
          color: #2c3e50;
          h2{
            font-size: 3rem;
            font-weight: bolder;
          }
        }
      }
    }
  }
}
</style>
