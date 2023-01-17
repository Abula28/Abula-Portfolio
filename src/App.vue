<template>
  <Navigation  />
  <Home  />
  <Skill />
  <Portfolio />
  <Contact />
</template>


<script>
  export default {
    components: {
      Navigation,
      Home,
      Skill,
      Portfolio,
      Contact
    }
  }

  import Navigation from './components/Navigation.vue'
  import Home from './components/Home.vue'
  import Skill from './components/Skill.vue'
  import Portfolio from './components/Portfolio.vue'
  import Contact from './components/Contact.vue'
</script>


<style lang="scss" scoped>
section{
  overflow: hidden;
}
.navBar{
  position: fixed;
}

</style>
