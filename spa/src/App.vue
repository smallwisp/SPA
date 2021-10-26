<template>
  <div id="app">
    <div class="header">
      <div class="header__container container">
        <h1 class="header__converter"><a href="#" class="header__link">{{converter}}</a></h1>
        <h1 class="header__briefcase"><a href="#" class="header__link">{{briefcase}}</a></h1>
      </div>
    </div>
    <!-- /.header -->
    <div class="currency container">
      <div class="currency__block currency__block_first">
        <span class="currency__choose">Выберите валюту</span>
        <select name="" id="" class="currency__select">
          <option value="">Bitcoin (BTC)</option>
          <option value="">Ethereum (ETH)</option>
          <option value="">US dollar (USD)</option>
        </select>
        <input
          v-bind:value="currencyInput"
          @input="currencyInput = $event.target.value"
          class="currency__input" 
          type="text"
          placeholder="Введите сумму">
      </div>
      <div class="currency__block second">
        <span class="currency__choose">Выберите валюту</span>
        <select name="" id="" class="currency__select"
          v-bind:value="currencySelect"
          @change="currencySelect = $event.target.value"
        >
          <option value="">Bitcoin (BTC)</option>
          <option value="">Ethereum (ETH)</option>
          <option value="">US dollar (USD)</option>
      </select>
      <input 
        v-bind:value="currencyOutput"
        class="currency__input currency__output" 
        type="text"
        placeholder="0.00" 
        disabled="">
      </div>
    </div>
    <!-- /.currency -->
    <div class="graph container">
      <div class="graph__heading"><h2 class="graph__text">График изменения курса криптовалюты за последние 14 дней</h2></div>
      <div class="graph__choose">
        <!-- <div class="currency__choose"> -->
          <span class="currency__choose">Выберите валюту</span>
          <select name="" id="" class="currency__select">
            <option value="">Bitcoin (BTC)</option>
            <option value="">Ethereum (ETH)</option>
            <option value="">US dollar (USD)</option>
          </select>
        <!-- </div> -->
      </div>
    </div>
    <!-- /.graph -->
    <!-- <router-view/> -->
  </div>
  <!-- /.app -->
</template>

<script>
export default {
  data() {
    return {
      converter: 'Конвертер валют',
      briefcase: 'Валютный портфель',
      currencyInput: '',
      currencyOutput: '',
      currencySelect: '',
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
  .header {
    /* margin-top: 50px;
    margin-bottom: 50px; */
    display: flex;
    justify-content: center;
  }
  .container {
    max-width: 1170px;
    margin: auto;
    // width: 90%;
    display: flex;
    justify-content: center;
  
  }
  .header__container {
    margin-top: 50px;
    margin-bottom: 50px;
    /* display: flex;
    justify-content: center; */
  }
  .header__converter {
    margin-right: 10px;
  }
  .header__converter::after {
    content: '|';
    margin-left: 10px;
  }
  .header__link, .header__link {
    color: #fff;
  }
  // header style
  .currency {
    margin-bottom: 50px;
  }
  .currency__block_first {
    margin-right: 30px;
  }
  .currency__select {
    cursor: pointer;
    background: rgba(255, 255, 255, 0.35);
    border: 1px solid rgba(255, 255, 255, 0.5);
    color: #fff;
    padding: 15px;
    width: 250px;
    border-radius: 10px;
    font-size: 18px;
  }
  .currency__block {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
  .currency__choose {
    margin-bottom: 10px;
  }
  .currency__input {
    margin-top: 20px;
    padding: 15px;
    width: 250px;
    border-radius: 10px;
    font-size: 18px;
  }
  // currency style
  .graph {
    display: flex;
    flex-direction: column;
  }
  .graph__text {
    margin-bottom: 30px;
    text-align: center;
  }
  .graph__choose {
    display: flex;
    flex-direction: column;
    align-self: start;
    align-items: center;
    // justify-content: center;
  }
  // graph style
  
</style>
