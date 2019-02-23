<template>
    <div>
        <input class="login-input" type="text" v-model="userName">
        <input type="button" :value="userName" @click="login">
        <div>{{testName}}</div>
    </div>
</template>

<script>
export default {
    name: 'Login',
    data () {
        return {
            userName: '',
            buttonText: '登录'
        }
    },
    computed: {
        testName () {
            return `${this.userName}-2`
        }
    },
    methods: {
        login () {
            const formData = {
                userName: this.userName
            }
            const res = this.$api.Accont.login(formData)

            if (res.code === 1) {
                this.$router.replace('/about')
            }
        }
    }
}
</script>

<style scoped>
.login-input {
    border: 10px solid rgb(180, 23, 23);
}

</style>
