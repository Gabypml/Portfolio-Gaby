<template>
  <div class="inner">
    <div class="wrapper">
      <div class="items">
        <div class="items__phrase">
          <h2> Vous avez aimé mon portfolio ? <br> <span class="fleche">→</span> N'hésitez pas à me <span><a href="mailto:Gaby_pombo.monteiro.leonor@hotmail.com?subject=Mail Du Portfolio">contacter !</a></span> </h2>
        </div>
      </div>
      <div class="madewith">
        <p>Fait avec <span> 🧡 </span> par Gaby Pombo © </p>
      </div>
    </div>
  </div>
</template>
<script>
export default {

}
</script>

<style lang="scss" scoped>
.inner{
  @include inner
  .wrapper{
    @include wrapper
    .items{
      padding-top: 10rem;
      padding-bottom: 5rem;

      &__phrase{

        h2{
          color:  #2c3e50;
          font-weight: lighter;
          font-size: 3rem;
          span{
            font-weight: normal;
            a{
              text-decoration: none;
              color:  #2c3e50;
              &:hover{
                font-weight: bolder;
              }
            }
          }
        }
      }
    }
    .madewith{
      border-top: 1px solid #f7e7d9;
      p{
        padding-top: 2rem;
        display: flex;
        align-items: center;
        justify-content: center;
        span{
          transform: scale(1);
          animation: pulse-black 2s infinite;
          @keyframes pulse-black {
            0% {
              transform: scale(1.3);
              box-shadow: 0 0 0 0 rgba(236, 154, 29, 0.7);
            }

          }
        }
      }
    }
  }
}
</style>
