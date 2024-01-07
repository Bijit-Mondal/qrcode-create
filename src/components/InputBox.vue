<template>
  <div class="input-box">
    <vs-input label-placeholder="Enter the URL" size="large" v-model="input_value"/>
    <vs-button @click="generateQR" color="#8C5E58" type="filled">Generate QR</vs-button>
  </div>
  <div class="output" v-if="output">
    <qrcode-vue :value="input_value" :size="size" level="H" />
  </div>
</template>

<script>
import QrcodeVue from 'qrcode.vue'
export default {
  name: 'InputBox',
  components: {
    QrcodeVue,
  },
  data() {
    return {
      input_value: '',
      size: 140,
      output: false,
    }
  },
  methods: {
    generateQR() {
      if(this.input_value!=''){
        this.output = !this.output;
      }else{
        this.$vs.notify({title:'Error',text:'Enter a URL'})
      }
    },
  },
}
</script>

<style scoped>
.input-box {
  display: flex;
  align-items: center;
  justify-content: center;
}

/* Add styles to separate vs-input and vs-button */
.vs-input {
  margin-top: 2px !important;
  margin-right: 10px; /* Adjust as needed for spacing between the elements */
}
.output {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 10px;
}
</style>
