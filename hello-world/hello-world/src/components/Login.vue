<template>
  <div>
    <div>
      <input class="login-name" type="text" v-model="userName">
    </div>
    <div>
      <input class="login-psd" type="text" v-model="psd">
    </div>
    <div>
      <input type="button" value="登陆" @click="login">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Login',
  data () {
    return {
      userName: '',
      psd: ''
    }
  },
  methods: {
    login () {
      if (this.userName !== '' && this.psd !== '') {
        this.$router.push('/')
        alert('I am fine')
      } else {
        alert('TMD, You must give me sth')
      }
    }
  }
}
</script>

<style lang="scss">
.login-name {
  border: 1px solid rgb(180, 23, 23);
}
</style>
