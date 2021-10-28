<template>
  <div id="app">
    <converter/>
    <graph/>
    <!-- <router-view/> -->
  </div>
  <!-- /.app -->
</template>

<script>
import converter from "@/components/converter";
import graph from "@/components/graph";

export default {
  components: {
    converter, graph
    
  },

  data() {
    return {
      converter: 'Конвертер валют',
      briefcase: 'Валютный портфель',
      currencyInput: '',
      currencyOutput: '',
      currencySelectInput: 'Bitcoin (BTC)',
      currencySelectOutput: 'US dollar (USD)',
      graphSelect: 'Bitcoin (BTC)',
    }
  },

  methods: {
    
  }
}
</script>

<style lang="scss">
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  body {
    // background-color: #0b3102cb;
     background: linear-gradient(45deg, rgba(16, 17, 15, 0.815) 0%, #0b3102cb 85.62%);
    font-family: 'Roboto', sans-serif;
    color: #fff;
  }
  #app {
    background: linear-gradient(45deg, rgba(16, 17, 15, 0.815) 0%, #0b3102cb 85.62%), url('./img/crypto-bg.jpg') no-repeat center top / cover;
  }
  .container {
    max-width: 1170px;
    margin: auto;
    // width: 90%;
    display: flex;
    justify-content: center;
  
  }

  // currency style
  
  
</style>
