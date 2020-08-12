<template>
  <div class="navBar">
    <div class="navBar__items">
      <div class="reseaux">
        <a href="https://www.instagram.com"><img src="@/assets/insta.png" class="reseau" alt="Logo instagram"></a>
        <a href="https://www.linkedin.com/in/gaby-pombo/"><img src="@/assets/linkedin.png" class="reseau" alt="Logo Linkedin"></a>
      </div>
      <ul class="link">
        <li v-for="(item, index) in items" :key="'menu-' + index">
          <a class="menu_item" v-scroll-to="item.link" :href="item.link">{{ item.message }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
  data: () => {
    return {
      items: [
        { message: 'Présentation', link: '#ThePresentation' },
        { message: 'Réalisations', link: '#MesRealisations' },
        { message: 'Contact', link: '#contact' }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
html{
   scroll-behavior: smooth;

.navBar__items{
  display: flex;
  padding-top: 1rem;
  padding-bottom: 2rem;

}
.link{

  list-style: none;
  display: flex;
  align-items: center;
  margin-left: auto;
}
li{
   @include media('small'){
    padding-right: 1.5rem;
  }
  padding-right: 3rem;
}
.menu_item{
  @include media('small'){
    font-size: 1.4rem;
  }
  font-size: 1.6rem;
  font-weight: lighter;
  text-decoration: none;
  color: #2c3e50;
  &:hover{
  border-bottom: 1.5px solid #f7e7d9;

}

}

.reseau{
  max-width: 3rem;
  padding-top: 1rem;
  padding-right: 0.3rem;
}
}
</style>
