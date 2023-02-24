<template>
  <div class="sighin">
    <p>username :{{ username }}</p>
    <input type="text" v-model="username" />
    <p>password :{{ password }}</p>
    <input type="text" v-model="password" />
    <p>province :{{ province }}</p>
    <select v-model="province">
      <option value="">please select</option>
      <option value="Tokyo">Tokyo</option>
      <option value="Osaka">Osaka</option>
      <option value="Fukuoka">Fukuoka</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "SignIn",
  data() {
    return {
      username: "",
      password: "",
      province: "",
    };
  },
};
</script>
