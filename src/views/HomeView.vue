<template>
  <div class="home-view">
    <TheIntro/>
    <ThePresentation/>
    <MesRealisations/>
    <MesCompetences/>
    <ContactezMoi/>
  </div>
</template>

<script>
import TheIntro from '@components/Homepage/TheIntro.vue'
import ThePresentation from '@components/Homepage/ThePresentation.vue'
import MesRealisations from '@components/Homepage/MesRealisations.vue'
import MesCompetences from '@components/Homepage/MesCompetences.vue'
import ContactezMoi from '@components/Homepage/ContactezMoi.vue'

export default {
  name: 'HomeView',
  components: {
    TheIntro,
    ThePresentation,
    MesRealisations,
    MesCompetences,
    ContactezMoi
  },
  computed: {},
  created () {},
  methods: {}
}
</script>
<style lang="scss" scoped>
.home-view{
  background-color: #f6e7d9;
}
</style>
