<template>
<div class="hello">
	<div>
		<label for="MyUserName">账号</label>
		<input type='text' v-model.trim="MyUserName" id="MyUserName"
     placeholder="账号" @blur="onUsernameBlur">
     <span class="error">{{ UserNameError }}</span>
	</div>
	<div>
	<label for="MyPassword">密码</label>
		<input type='password' v-model.trim="MyPassword" id="MyPassword"
    placeholder="密码"  @blur="onPasswordBlur">
     <span class="error">{{ PasswordError }}</span>
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
	<button v-on:click="subMit">提交</button>
</div>
</template>
<script>
export default {
  data () {
    return {
      MyUserName: '',
      MyPassword: '',
      RememberMe: false,
      Sex: '',
      UserNameError: '',
      PasswordError: ''
    }
  },
  methods: {
    onUsernameBlur: function () {
      if (this.MyUserName.length === 0) {
        this.UserNameError = '账号不能为空'
      } else {
        this.UserNameError = ''
      }
    },
    onPasswordBlur: function () {
      if (this.MyPassword.length === 0) {
        this.PasswordError = '密码不能为空'
      } else {
        this.PasswordError = ''
      }
    },
    subMit: function () {
      this.onUsernameBlur()
      this.onPasswordBlur()
      return this.isValid()
    },
    isValid: function () {
      if (this.UserNameError.length === 0 && this.PasswordError.length === 0) {
        return true
      }
      return false
    }
  }
}
</script>

<style>
.hello {
  color: #42b983;
}
.hello div {
  margin-left: 0px;
}
.error{
  color: #ca3131;
}
</style>
