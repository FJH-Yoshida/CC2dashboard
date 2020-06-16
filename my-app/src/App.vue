<template>
<body>
  <div class="app" id="app">
    <Index v-for="post in posts01"
              v-bind:key="post.id"
              v-bind:title="post.title"
              v-bind:eval="post.eval"
              v-bind:rate="post.rate"
              v-bind:value="post.value"
              v-bind:unit="post.unit"
    ></Index>
  </div>
  <div>
    <Table  v-for="post in posts02"
              v-bind:key="post.id"
              v-bind:title="post.title"
              v-bind:perform="post.perform"
              v-bind:comp="post.comp"
              v-bind:growth="post.growth"
              v-bind:value="post.value"
              v-bind:eval="post.eval"
    ></Table>
  </div>
</body>
</template>
<script>
import Index from './components/Index'
import Table from './components/Table'

export default {
  components: {
    Index,
    Table
  },

  data: function () {
    return {
      posts01: [
        {id: 1, title: '医業収益', eval: 'A', rate: '+12.3', value: '301', unit: '百万円'},
        {id: 2, title: '診療単価', eval: 'C', rate: '-3.6', value: '6,209', unit: '円'},
        {id: 3, title: '延患者数', eval: 'C', rate: '-3.6', value: '832', unit: '人'},
        {id: 4, title: '平均在院日数', eval: 'B', rate: '+3.2', value: '12.3', unit: '日'},
        {id: 5, title: '病院稼働率', eval: 'A', rate: '+12.2', value: '82.3', unit: '%'},
        {id: 6, title: '外来/入院比', eval: 'B', rate: '+3.2', value: '171', unit: '%'}
      ],
      posts02: [
        {id: 1, title: '医業収益', perform: '700万円', comp: '610万円', growth: '13.2', value: '550万円', eval: 'A'},
        {id: 2, title: '外来収益', perform: '350万円', comp: '330万円', growth: '4.2', value: '250万円', eval: 'B'},
        {id: 3, title: '入院収益', perform: '350万円', comp: '6,000円', growth: '1.2', value: '300万円', eval: 'C'}
      ]
    }
  }
}
</script>
<style scoped>
body{
  font-family: Meiryo, 'メイリオ', Tahoma, Verdana, 'ヒラギノ角ゴ Pro W3', 'Hiragino Kaku Gothic Pro', Osaka, 'ＭＳ Ｐゴシック', 'MS PGothic', sans-serif;
}

div.app{
  display: flex;
  flex-wrap: wrap;
}
</style>
