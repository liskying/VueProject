<template>
<div class="hello">
	<div>
		<label for="UserName">账号</label>
		<input type='text' v-model.trim="UserName" id="UserName" placeholder="账号" >
	</div>
	<div>
	<label for="Password">密码</label>
		<input type='password' v-model.trim="Password" id="Password" placeholder="密码">
	</div>
	<div>
		<label for="Sex">性别</label>
		<select v-model.trim="Sex" name="Sex">
		    <option value="">性别</option>
		    <option value="1">先生</option>
		    <option value="2">女士</option>
	  	</select>
	</div>
	<div>
		<label for="RememberMe">记住我</label>
		<input type="checkbox" id="RememberMe" v-model="RememberMe">
	</div>
	<div>
	{{ 
		if(UserName.length===0){
			"账号不能为空"
		}
		if(UserName.length===0){
			"密码不能为空"
		}	
	}}
	</div>
</div>
</template>
<script>
export default {
  data	() {
    return {
      UserName: '',
      Password: '',
      RememberMe:	false,
      Sex:	''
    }
  }
}
</script>

<style>
.hello {
  color: #42b983;
}
.hello div{
  margin-left:0px;
}
</style>
