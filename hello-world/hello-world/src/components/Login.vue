<template>
  <div>
    <div>
      <input class="login-input" type="text" v-model="userName">
    </div>
    <div>
      <input class="login-input" type="text" v-model="psd">
    </div>
    <div>
      <input type="button" value="登陆" @click="login">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Login',
  methods: {
    login () {
      if (this.userName !== '' && this.psd !== '') {
        this.$router.push('/')
        alert('I am fine')
      }
    }
  }
}
</script>
