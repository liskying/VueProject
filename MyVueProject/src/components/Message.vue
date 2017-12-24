<template>
<div class="message">
    <label for="r1">修改颜色</label><input type="checkbox" v-model="class1" id="r1">
	<div v-html='Message' v-bind:class="{'class1': class1}">

	</div>
</div>
</template>
<script>
export default {
  data () {
    return {
      Message: '<div></div>',
      class1: false
    }
  }
}
</script>

<style>
.message {
  font-size:15pt;
}
.class1{
  background: #444;
  color: #eee;
}
</style>
