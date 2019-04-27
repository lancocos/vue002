<template>
    <div>
        <div  v-show="!status">
            <div><input type="text" v-model="user.username" ></div>
            <div><input type="text" v-model="user.password"></div>
            <div><input type="checkbox" v-model="user.remember" >remember me?</div>
            <div><input type="button" value="Login" @click="Login" ></div>
            <div><router-link to="register">Register</router-link></div>
        </div>
        <div v-show="status">
            <div>welcome {{user.username}}<a @click.prevent="logout">logout</a></div>
        </div>
    </div>
</template>
<script>
export default{
  name: 'Login',
  data: function () {
    return {
      user: {},
      status: false
    }
  },
  methods: {
    Login: function () {
      if (this.user.username === 'admin' && this.user.password === 'admin') {
        this.status = true
      }
    },
    logout: function () {
      this.user = {}
      this.status = false
    }
  }
}
</script>
