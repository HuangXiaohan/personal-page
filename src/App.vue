<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <div class="container">
     <button type="button" class="btn btn-success">Success</button>
     <button type="button" class="btn btn-info">Info</button>
     <button type="button" class="btn btn-warning">Warning</button>
  </div> -->
  <ProfileHeader></ProfileHeader>
  <div class="p-5">
    <ExperienceSection></ExperienceSection>
  </div>
</template>

<script>
import ProfileHeader from './components/ProfileHeader.vue'
import ExperienceSection from './components/ExperienceSection.vue'

export default {
  name: 'App',
  components: {
    ProfileHeader,
    ExperienceSection
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
