<template>
  <div class="container">
    <b-card
      title="欢迎登录"
      img-src="https://via.placeholder.com/150"
      img-alt="Image"
      img-top
    >
      <b-form @submit.prevent="handleSubmit">
        <b-form-group id="input-group-1" label="用户名:" label-for="input-1">
          <b-form-input
            id="input-1"
            v-model="username"
            type="text"
            required
          ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-2" label="密码:" label-for="input-2">
          <b-form-input
            id="input-2"
            v-model="password"
            type="password"
            required
          ></b-form-input>
        </b-form-group>

        <b-button type="submit" variant="primary">登录</b-button>
      </b-form>
    </b-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: "",
      password: "",
    }
  },
  methods: {
    handleSubmit() {
      if (this.username && this.password) {
        alert("登录成功！")
        // 在实际应用中，这里可以发送 AJAX 请求到服务器验证登录信息
      } else {
        alert("请输入用户名和密码！")
      }
    },
  },
}
</script>
