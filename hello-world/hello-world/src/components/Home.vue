<template>
  <div class="home">
    <p>This is Home page</p>
    <input type="button" value="开始登陆" @click="beginlogin">
  </div>
</template>

<script>
export default {
  name: 'Home',
  methods: {
    beginlogin () {
      // this.$router.push('/login')
      window.open('/login')
    }
  }
}
</script>
