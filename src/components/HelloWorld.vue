<template>
    <div class="hello">
      <h1>{{ msg }}</h1>
      <vs-button color="warning" type="filled">Warning</vs-button>
      <qrcode-vue :value="value" :size="size" level="H" />
    </div>
  </template>
  
  <script>
  import QrcodeVue from 'qrcode.vue'
  
  export default {
    name: 'HelloWorld',
    data() {
      return {
        value: 'https://youtube.com',
        size: 300,
      }
    },
    components: {
        QrcodeVue,
    },
    props: {
      msg: String
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
  </style>
  