<template>
  <form class="form" @submit.prevent="onSubmit">
    <label for="fname">
      First Name
      <input id="fname" name="fname" />
    </label>

    <label for="lname">
      Last Name
      <input id="lname" name="lname" />
    </label>

    <button type="submit">Submit</button>
  </form>
</template>

<script>
import userStore from "../store/user.js";

export default {
  methods: {
    onSubmit({ target }) {
      const data = new FormData(target);
      const user = Object.fromEntries(data);
      userStore.user = user;
    }
  }
};
</script>

<style>
.form {
  max-width: 600px;
  margin: 0 auto;
}
input {
  display: block;
  width: 100%;
  margin-bottom: 1rem;
}
</style>
