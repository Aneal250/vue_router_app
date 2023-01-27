<template>
  <div class="login">
    <form @submit.prevent="login" class="form">
      {{ username }}
      <h1>Login</h1>
      <label for="username">Username</label>
      <input v-model="username" name="username" type="text" class="input" />
      <label for="password">password</label>
      <input v-model="password" name="password" type="text" class="input" />
      <button class="btn">Login</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: "",
      password: "",
    };
  },
  methods: {
    login() {
      window.user = this.username;
      this.$router.push({ name: "protected" });
    },
  },
};
</script>
