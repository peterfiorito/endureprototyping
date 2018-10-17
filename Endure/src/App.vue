<template>
  <div id="app">
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.4.1/css/all.css"
      integrity="sha384-5sAR7xN1Nv6T6+dT2mhtzEpVJvfS3NScPQTrOxhwjIuvcA67KV2R5Jz6kr4abQsz"
      crossorigin="anonymous">
    <MenuBar />
    <MainHeader />
    <div class="app__application-form-envelope">
      <ApplicationForm />
    </div>
    <FirstFooter />
  </div>
</template>

<script>
import MenuBar from './components/MenuBar.vue'
import MainHeader from './components/MainHeader.vue'
import ApplicationForm from './components/ApplicationForm.vue'
import FirstFooter from './components/FirstFooter.vue'
export default {
  name: 'App',
  components: {
    MenuBar,
    MainHeader,
    ApplicationForm,
    FirstFooter
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body{
  margin: 0px;
}
.app__application-form-envelope {
  background-color: #eeeeee85;
  margin-top: 0px
}
</style>
