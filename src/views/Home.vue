<template>
  <div class="home">
    <img class="drag" alt="Vue logo" src="https://static.xx.fbcdn.net/rsrc.php/y8/r/dF5SId3UHWd.svg">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import $ from 'jquery' 
import 'jquery-ui-dist/jquery-ui'  
window.jQuery = $ 
require('jquery-ui-touch-punch')

export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  mounted () {     $('.drag').draggable();   } 
}
</script>

<style type="text/css" scoped="">
	img {
		width: 420px;
	}
</style>
