<template>
  <div>
    <div v-if="user">
      Welcome {{ fullName }}!
      <button @click="logout">Logout</button>
    </div>

    <img alt="Vue logo" src="../assets/logo.png" />
  </div>
</template>

<script>
import userStore from "../store/user.js";

export default {
  computed: {
    user: () => userStore.user,

    fullName() {
      const user = this.user;
      if (!user) return "";
      return `${user.fname} ${user.lname}`;
    }
  },

  methods: {
    logout() {
      userStore.user = null;
    }
  }
};
</script>
