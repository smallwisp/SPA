<template>
    <div>
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
        <select name="" id="" class="currency__select"
        v-model="post.currencySelectInput">
          <option>Bitcoin (BTC)</option>
          <option>Ethereum (ETH)</option>
          <option>US dollar (USD)</option>
        </select>
        <input
          v-bind:value="post.currencyInput"
          @input="post.currencyInput = $event.target.value"
          class="currency__input" 
          type="text"
          placeholder="Введите сумму">
      </div>
      <div class="currency__block second">
        <span class="currency__choose">Выберите валюту</span>
        <select name="" id="" class="currency__select"
          v-model="post.currencySelectOutput"
        >
          <option>Bitcoin (BTC)</option>
          <option>Ethereum (ETH)</option>
          <option>US dollar (USD)</option>
      </select>
      <input 
        v-bind:value="post.currencyOutput"
        class="currency__input currency__output" 
        type="text"
        placeholder="0.00" 
        disabled="">
      </div>
    </div>
    <!-- /.currency -->
    </div>
</template>

<script>
export default {
    data() {
        return {
            post: {
                currencyInput: '',
                currencyOutput: '',
                currencySelectInput: 'Bitcoin (BTC)',
                currencySelectOutput: 'US dollar (USD)',
            },
            converter: 'Конвертер валют',
            briefcase: 'Валютный портфель',
        }
  },
}
</script>

<style scoped lang="scss">
      .header {
    /* margin-top: 50px;
    margin-bottom: 50px; */
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
</style>