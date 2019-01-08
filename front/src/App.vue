<template>
<div id="app">
  <Header/>
  <MainContent/>
</div>

</template>

<script>
import Header from './components/Header.vue'
import MainContent from './components/MainContent.vue'

export default {
  name: 'app',
  components: {
    Header,
    MainContent
  }
}
</script>

<style>

</style>
