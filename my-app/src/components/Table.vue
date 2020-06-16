<template>
 <div class='table'>
   <div class='table_title'>
     <div class="block_title">評価指標</div>
     <div class="block_title">実績値</div>
     <div class="block_title">比較値</div>
     <div class="block_title">成長率</div>
     <div class="block_title">ベンチマーク値</div>
     <div class="block_title">ベンチマーク評価</div>
   </div>
   <div class='table_line'>
     <div class="block_line">{{title}}</div>
     <div class="block_line">{{perform}}</div>
     <div class="block_line">{{comp}}</div>
     <div class="block_line">{{growth}}</div>
     <div class="block_line">{{value}}</div>
     <div class="block_line">{{eval}}</div>
   </div>
 </div>
</template>
<script>
export default {
  props: ['title', 'perform', 'comp', 'growth', 'value', 'eval']
}
</script>
<style scoped>
div.table_title{
  display: table;
}

div.block_title{
  display: table-cell;
	border: solid 1px #999;
	width: 16%;
}

div.table_line{
  display: table;
}

div.block_line{
  display: table-cell;
	border: solid 1px #999;
  width: 16%;
}

</style>
