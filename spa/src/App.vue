<template>
  <div id="app">
    <div class="header">
      <h1 class="header-converter"><a href="#" class="converter-link">{{converter}}</a></h1>
      <h1 class="header-briefcase"><a href="#" class="briefcase-link">{{briefcase}}</a></h1>
    </div>
    <div class="currency container">
      <div class="currency-block first">
        <span class="currency-choose">Выберите валюту</span>
        <select name="" id="" class="select currency">
          <option value="">Bitcoin (BTC)</option>
          <option value="">Ethereum (ETH)</option>
          <option value="">US dollar (USD)</option>
      </select>
      <input class="currency-input" type="text" placeholder="Введите сумму">
      </div>
      <div class="currency-block second">
        <span class="currency-choose">Выберите валюту</span>
        <select name="" id="" class="select currency">
          <option value="">Bitcoin (BTC)</option>
          <option value="">Ethereum (ETH)</option>
          <option value="">US dollar (USD)</option>
      </select>
      <input class="currency-input" type="text" placeholder="0.00" disabled="">
      </div>
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  data() {
    return {
      converter: 'Конвертер валют',
      briefcase: 'Валютный портфель'
    }
  }
}
</script>

<style lang="scss">
  * {
    box-sizing: border-box;
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
    margin-top: 50px;
    margin-bottom: 50px;
    display: flex;
    justify-content: center;
  }
  .header-converter {
    margin-right: 10px;
  }
  .converter-link, .briefcase-link {
    color: #fff;
  }
  .converter-link::after {
    content: '|';
    margin-left: 10px;
  }
  .container {
    max-width: 1170px;
    margin: auto;
    // width: 90%;
    display: flex;
    justify-content: center;

  }
  .first {
    margin-right: 30px;
  }
  .select {
    cursor: pointer;
    background: rgba(255, 255, 255, 0.35);
    border: 1px solid rgba(255, 255, 255, 0.5);
    color: #fff;
    padding: 18px;
    width: 250px;
    border-radius: 10px;
    font-size: 18px;
  }
  .currency-block {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
  .currency-choose {
    margin-bottom: 10px;
  }
  .currency-input {
    margin-top: 20px;
    padding: 18px;
    width: 250px;
    border-radius: 10px;
    font-size: 18px;
  }
  
</style>
