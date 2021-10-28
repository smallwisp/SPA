<template>
    <div>
        <div class="graph container">
      <div class="graph__heading"><h2 class="graph__text">График изменения курса криптовалюты за последние 14 дней</h2></div>
      <div class="graph__choose">
        <!-- <div class="currency__choose"> -->
          <span class="currency__choose">Выберите валюту</span>
          <select name="" id="" class="currency__select"
          v-model="post.graphSelect">
            <option>Bitcoin (BTC)</option>
            <option>Ethereum (ETH)</option>
            <option>US dollar (USD)</option>
          </select>
        <!-- </div> -->
      </div>
    </div>
    <!-- /.graph -->
    </div>
</template>

<script>
export default {
    data() {
        return {
            post: {
                graphSelect: 'Bitcoin (BTC)'
            },
        }
  },
}
</script>

<style scoped lang="scss">
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
  .currency__choose {
    margin-bottom: 10px;
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
  // graph style
</style>