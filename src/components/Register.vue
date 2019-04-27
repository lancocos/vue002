<template>
<div id="regbox">
    <div><input type="text" v-model="user.username" ></div>
    <div><input type="password" v-model="user.password"></div>
    <div><input type="checkbox" v-model="user.remember" >remember me?</div>
    <div><input type="button" value="register" @click="register" ></div>
    <div><router-link to="Login">Login</router-link></div>
</div>
</template>
<script>
export default{
  name: 'Register',
  data: function () {
    return {
      user: {}
    }
  },
  methods: {
    register: function () {
      console.log(this.user)
    }
  }

}
</script>
<style scoped>
#regbox{
    border:1px solid #ddd;
    padding:10px;
}
#regbox>div{
    margin-bottom: 10px;
}
#regbox>div>input[type="text"],#regbox>div>input[type="password"]{
    border:1px solid #39af5c;
    height:20px;
}
</style>
