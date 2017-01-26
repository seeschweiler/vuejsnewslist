<template>
  <div class="container" id="app">
    
    <div class="alert alert-warning alert-dismissible" role="alert">
      <button type="button" class="close" data-dismiss="alert" aria-label="Close"><span aria-hidden="true">&times;</span></button>
      <strong><a href="http://codingthesmartway.com/courses/vuejs2-complete-guide" target="_blank">[ONLINE COURSE] - Vue.js 2 - The Complete Guide</a></strong> +++ Understand the Theory behind Vue.js and use it in Real Projects. +++  Build amazing Vue.js Applications - all the Way from Small and Simple Ones up to Large Enterprise-level Ones +++ Leverage Vue.js in both Multi- and Single-Page-Applications (MPAs and SPAs) +++
    </div>
    
    <SourceSelection v-on:sourceChanged="sourceChanged"></SourceSelection>
    <Newslist v-bind:source="source"></Newslist>
    
    <div class="footer">
      <p>&copy <a href="http://codingthesmartway.com" target="_blank">CodingTheSmartWay.com</a> | <a href="http://codingthesmartway.com/imprint" target="_blank">Imprint</a></p>
    </div>
  </div>
</template>

<script>
import Newslist from './components/Newslist'
import SourceSelection from './components/SourceSelection'

export default {
  name: 'app',
  components: {
    Newslist,
    SourceSelection
  },
  data () {
    return {
      source: ""
    }
  },
  methods: {
    sourceChanged: function (source) {
      this.source = source;
    }
  }
}
</script>

<style>
  #app {
    padding-top: 20px
  }
</style>
