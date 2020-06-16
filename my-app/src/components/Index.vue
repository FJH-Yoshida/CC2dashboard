<template>
 <div class='index'>
   <span class='title'>{{title}}</span>
   <div class='main'>
     <div class="eval" v-bind:style="{backgroundColor:resultColor}">
       <span class='eval'>{{eval}}評価</span>
     </div>
     <div class='value'>
       <span class='value'>{{value}}</span>
       <div class='rate'>
         <span class = 'rate' v-bind:style="{color:resultColor}">{{rate}}%</span>
         <div class='unit'>
           <span class='unit'>({{unit}})</span>
         </div>
       </div>
     </div>
   </div>
 </div>
</template>
<script>
export default {
  props: ['title', 'rate', 'eval', 'value', 'unit'],

  data () {
    var numRate = parseFloat(this.rate)
    if (numRate >= 10) {
      return {
        resultColor: '#7fffd4'
      }
    } else if (numRate >= 0 && numRate < 10) {
      return {
        resultColor: '#adff2f'
      }
    } else if (numRate > -10 && numRate < 0) {
      return {
        resultColor: '#ffd700'
      }
    } else if (numRate < -10) {
      return {
        resultColor: '#ff4500'
      }
    }
  }
}
</script>
<style scoped>
div.index{
  background-color: #fff;
  box-shadow: 0 32px 30px -30px rgba(53, 47, 47, 0.15);
  margin: 2px;
  padding: 5px;
  width: 30%;
}

span.title{
  display: flex;
  left:10px;
  font-size: 17px;
  border-left: thick solid #1e90ff;
  padding-left: 10px;
}

span.rate{
  font-weight: bold;
  padding: 5px;
  top: 30px;
  left: 70px;
}

div.eval{
  float: right;
  color: #fff;
  font-size: 20px;
  margin: 0px;
  padding: 5px;
  border-radius: 5px;
}

div.value{
  display: flex;
}

span.value{
  font-size: 30px;
  font-weight: bold;
  font-style: oblique;
}

span.unit{
  font-size: 15px;
  font-weight: bold;
}
</style>
