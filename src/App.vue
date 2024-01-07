<template>
  <NavBar/>
  <div id="body">
    <div style="display: flex;">
      <div id="logo">
        <img src="./assets/logo.png" id="logo"/>
      </div>
      <div style="padding: 10em;">
        <h1>QR Code Generator, Your QR Code Companion</h1>
      </div>
    </div>
    <InputBox/>
  </div>
</template>

<script>
import InputBox from './components/InputBox.vue'
import NavBar from './components/NavBar.vue'
export default {
  name: 'App',
  components: {
    InputBox,
    NavBar
  }
}
</script>
<style>
body, html {
  height: 100%;
  margin: 0;
  padding: 0;
}
#body{
  background-color: #BB9D99;
  width: 100vw;
  height: 100vh;
}
#logo{
  width:20em;
  height:20em;
  padding: 2em;
}
</style>
