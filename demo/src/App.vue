<template>
    <HeaderComponent />
    <HomeComponent/>
    <FooterComponent />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import HeaderComponent from './components/layouts/HeaderComponent.vue'
import HomeComponent from './components/user/HomeComponent.vue'
import FooterComponent from './components/layouts/FooterComponent.vue'

export default {   
  name: 'App',
  components: {
    HeaderComponent,
    HomeComponent,
    FooterComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  /* margin-top: 60px; */
}
</style>
